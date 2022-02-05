# Data pipeline

Docker pipeline that collects tweets and stores them in MongoDB, afterwards the sentiment of the tweets is analyzed and the results are stored in PostgreSQL
<br />
<br />
## What you need in addition to run the pipeline:
* Postgres password
* Twitter API credentials  
  **&rarr;** save your twitter credentials in a 'credentials.py' file inside the 'tweet_collector' folder  
<br />
## How to run the pipeline:
* Run the commands  
  `docker-compose build` which builds all container images  
  and   
  `docker-compose up` which starts the pipeline  
<br />

## While the pipeline is running:

### Access to MongoDB:
  - open a new terminal window and use the following command to access the database on MongoDB:   
    `docker-compose exec mongodb mongo`  
  - Then, in order to see your stored tweets type in the MongoDB shell:  
    `use twitter`  
    and   
    `db.tweets.find()`
    
### Access to PostgreSQL:


  
