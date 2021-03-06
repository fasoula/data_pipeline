# Data pipeline

Docker pipeline that collects tweets and stores them in MongoDB. Afterwards the sentiment of the tweets is analyzed and the results are stored in PostgreSQL. The Postgres database can then be connected to Metabase in order to generate visualizations and dashboards.  
In this repository you will find also in the folder 'visualization_of_sentiments_python' how to extract the tweets and save them in a csv file as well as a brief visualization in Python.  
<br />
## What you need in addition to run the pipeline:
* Postgres password
* Twitter API credentials  
  **&rarr;** save your twitter credentials in a 'credentials.py' file inside the 'tweet_collector' folder  

## How to run the pipeline:
* Run the commands  
  `docker-compose build` which builds all container images  
  and   
  `docker-compose up` which starts the pipeline      


## While the pipeline is running:

### Access to MongoDB:
  * open a new terminal window and use the following command to access the database on MongoDB:   
    `docker-compose exec mongodb mongo`  
  * Then, in order to see your stored tweets type in the MongoDB shell:  
    `use twitter`  
    and  
    `db.tweets.find()`
    
### Access to PostgreSQL:
  * open a new terminal window and use the following command to access the database in PostgreSQL:  
    `psql -U myusername -h 0.0.0.0 -p 5555 mydbname`  
    in this case  
    `psql -U postgres -h 0.0.0.0 -p 5555 tsla_tweets`


  
