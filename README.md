# [ElasticSearchBackedMicroService](http://franken-search-998065281595.s3-website-us-east-1.amazonaws.com/)
## Objective
### We need to find how often a word searched by the user was been used in the Mary Shelley's Frankenstein!

## Architecture
* A FrakenWords front end website asking for search words from users is hosted on AWS S3.
* All the chapters and letters from Frankenstein are uploaded in ElasticSearch
* Writing a lambda function which runs 'simple_query_string' query to retrieve total number of hits, their scores based on levenshtein distances and their respective locations.
* Frontend calling the endpoint of APIGateway which triggers the lambda function

## Architecture HLD
![alt text](https://github.com/Rajeshwarchennam/ElasticSearch/blob/master/ElasticSearchBackedMicroService.png)