# Data pipeline

Docker pipeline that collects tweets and stores them in MongoDB, afterwards the sentiment of the tweets is analyzed and the results are stored in PostgreSQL

## What you need in addition to run the pipeline:
* Postgres password
* Twitter API credentials
  --> save your twitter credentials in a 'credentials.py' file inside the 'tweet_collector' folder
  &rarr;
