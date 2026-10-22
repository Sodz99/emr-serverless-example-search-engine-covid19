# COVID-19 Data pipeline and Relevant Papers Search Engine
## Overall Structure
## EMR Serverless
EMR Serverless is used through `BOTO3` and `AWS Data Wrangler` libraries. The initial starting point to 
spin up a job is ``run_emr_serverless.py``. This file contains all the OPS required to spin up a 
spark job. Currently, it spins up a job defined in ``spark_job.py``. The general workflow is explained
below:

1 - **Copy Modules and Environment to S3 Bucket**: We copy the local `src` folder so all modules 
created are available to our spark job. We zip the src folder and upload it to S3 using AWS data Wrangler.
Also, in order to use custom libraries defined in the `requirements.txt` we have to create a copy of 
Python Virtual Environment and also make it available into S3. The caveat in here is that this environment
needs to be created using Amazon Linux, hence why the Docker Image is made available to create the file.
Run the command in the Docker Section Belo to create the file.

2 - **Create and/or Start EMR Serverless Application**: EMR Serverless jobs are contained within an
application. The latter contains all configuration for min and max amount of resources that we want to 
allocate for all of our jobs. A good practice is to create an application for each specific theme.
The code will create an application if an `APPLICATION_ID` is not provided from the `src/utils/consts.py` 
file


## Glue
Glue is used to create metadata for tables in Athena. ``src/processing/glue.py`` contains all 
required wrapper functions to read data from a S3 bucket and create Athena table
## Athena
## Lambda
## Docker
``` DOCKER_BUILDKIT=1 docker build --output . .```