# EMR Serverless Example to Build a Search Engine for COVID19

EMR Serverless Example to Build a Search Engine for COVID19 — AWS Data Engineering project.

## Overview
Serverless architecture is a method of developing and deploying applications and services without maintaining infrastructure. Your application is still running on servers, but AWS manages them all. You no longer need to provision, scale, and maintain servers to operate your applications, databases, and storage systems. Learn more about serverless computing by clicking here. Serverless architecture allows developers to focus on their core product rather than maintaining and administering servers or runtimes in the cloud or on-premises. This decreased overhead frees up time and resources for developers to focus on creating excellent solutions that scale and are dependable. We aim to create a search engine using the BM25 TF-IDF Algorithm that uses EMR Serverless for ad-hoc processing of a large amount of unstructured textual data. In this project, we will use different amazon services such as EMR Serverless, AWS S3, AWS Glue, Amazon Athena, etc. Once the data is processed using EMR Server

## Data
The COVID-19 Open Scientific Dataset was created in response to the COVID-19 epidemic by the White House and a consortium of top research organizations (CORD-19). The CORD-19 database contains more than a million research publications about COVID-19, SARS-CoV-2, and similar coronaviruses, including more than 400,000 full-text articles. With the help of current developments in natural language processing and other AI approaches, the research community at large can use this freely accessible information to produce fresh insights that will aid in the ongoing battle against this contagious disease. The medical research community is struggling to keep up with the tremendous acceleration of new coronavirus literature, which has increased the urgency for these techniques.

_Data is not included in this repository._

## Tech stack
➔ Language: Python ➔ Package: PySpark ➔ Services: AWS S3, AWS Glue, Amazon Athena, EMR Serverless

Amazon EMR Serverless: Amazon Elastic Map Reduce (EMR) Serverless offers a serverless runtime environment that makes it easier to run analytics programs that use the most recent open-source frameworks, such as Apache Spark and Apache Hive. Using EMR Serverless, there is no need to optimize, secure, configure, or operate clusters to run applications with these frameworks.

## How to run
```bash
pip install -r emr-serverless/requirements.txt
python emr-serverless/src/search/engine.py
```
Notebooks: [`main.ipynb`](emr-serverless/src/main.ipynb)

## Project structure
```
.gitignore
README.md
emr-serverless/
  .gitignore
  Dockerfile
  README.md
  requirements.txt
  src/
    main.ipynb
    processing/
    run_emr_serverless.py
    search/
    spark_job.py
    utils/
```

## Credits
Based on a ProjectPro guided project.
