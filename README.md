## **My RDS to S3 archiver README:** ##

## **What the script does:** ##

This ansible script checks for some archived RDS MySQL tables, backs them up to an AWS S3 bucket, and sends an alert via AWS SNS service (which in turn sends email) once done. 

The system also sends an alert via AWS SNS service if the script fails at any point during the process. 

## **Requirements:** ##
1. Packages:
*  boto,
*  ansible,
*  mysql-client-5.7,
*  mysql-client-core-5.7.

2. AWS services:
*  aws account,
*  RDS instance with MySql,
*  S3 bucket created,
*  SNS topic for sms and email configured.


## **How to run the script (linux shell):** ##

Edit the script to replace the variables ( replace the XXX with your own variable )


```
#!bash

ansible-playbook RDS_to_S3_archiver.yml -vvvv
```
