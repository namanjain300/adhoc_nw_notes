# Hadoop Framework

* HDFS
* YARN => Processing --admin / dev
* HIVE
* PIG => Structure data handling, dataware housing

* Sqoop => databse -> HDFS
* Apache Storm => Real time Data Processing

* Ambari => Web portal
* Hortonworks
* Cloudera => free / paid
 
* Apache spark

## Apache spark

* Data Processing
    * Storage -> own storage, HDFS use
    * Processing -> own processing, YARN
    * SQL Data -> apache sql (similar with HIVE - HQL)
    * Live Stream -> By default supported (as in apache storm)
    * AI/ML -> spark -> MLIB (HDFS -> apache mahout)
    * Analytics/Visual -> spark GraphX
    * spark -> R, JAVA, Python, Scala (Build Language)
    * Processinng is 10X times more faster of Apache Spark as compared to YARN
    * Databricks -> HDFS, S3, live, file [ DBFS (Databricks File System)]

# **Cloud**
Today's Topic
---
* Route53
* Auto Scalling

### **Auto Scalling**
* It is a Feature of AWS
* Automatically add or remove resources according to the usage of it
* Cloud Watch is the paid service of AWS which monitors billing and creating of resources
* SNS (Simple Notification Service) -> This services captures the notification or alarm and set the alarm if it exceeds the limit (limit -> which is created by user).
* Bootstraping
* Steps:-

    1.  Creating ELB
    2. Template
    ```
    #!/bin/bash
    yum install httpd php git -y
    systemctl start httpd
    systemctl enable httpd
    setenforce 0
    iptables -F # this will turn off firewall
    echo "Hello Adhoc" >/var/www/html/index.html
    cd /var/www/html
    git clone https://github.com/redashu/phpsampleapp
    mv phpsampleapp adhoc
    ```
    * For Deleting :- First Auto Scaling Group then Launch Configuration and then Load Balancer


