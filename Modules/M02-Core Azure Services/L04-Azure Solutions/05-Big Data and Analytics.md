
Data comes in all types of forms and formats. When we talk about Big Data, we're referring to large volumes of data. Data from weather systems, communications systems, imaging platforms, and many other scenarios generate large amounts of data. This amount of data becomes increasingly hard to make sense of, and make decisions around. The volumes are so large that traditional forms of processing and analysis are no longer appropriate. 

Open source cluster technologies have been developed, over time, to try to deal with these large data sets. Microsoft Azure supports a broad range of technologies and services to provide big data and analytic solutions. Some of the most common big data and analytic service types in Azure are Azure SQL Data Warehouse, HDInsight, and Data Lake Analytics.


### **Azure SQL Data Warehouse**

<p style="text-align:left;"><img src="../Linked_Image_Files/sqldatawharehouse.png" width="100" height="100" alt="Image representing SQL Data Warehouse"></p>

*Azure SQL Data Warehouse* is a cloud-based Enterprise Data Warehouse (EDW) that leverages MPP to run complex queries quickly across petabytes of data. You can use SQL Data Warehouse as a key component of a big data solution by importing big data into SQL Data Warehouse with simple PolyBase Transact-SQL (T-SQL) queries, and then use the power of MPP to run high-performance analytics. Once data is stored in SQL Data Warehouse, you can run analytics at massive scale. Compared to traditional database systems, analysis queries finish in seconds instead of minutes, or hours instead of days. See <a href="https://azure.microsoft.com/en-us/services/sql-data-warehouse/" target="_blank"><span style="color: #0066cc;" color="#0066cc">SQL Data Warehouse</span></a> for more details.


### **Azure HDInsight**

<p style="text-align:left;"><img src="../Linked_Image_Files/hdinsight.png" width="100" height="100" alt="Image representing Azure HDInsight"></p>

*Azure HDInsight* is a fully managed, open-source analytics service for enterprises. It is a cloud service that makes it easier, faster, and more cost-effective to process massive amounts of data. HDInsight allows you run popular open-source frameworks and create cluster types such as <a href="https://docs.microsoft.com/en-us/azure/hdinsight/spark/apache-spark-overview" target="_blank"><span style="color: #0066cc;" color="#0066cc">Apache Spark</span></a>, <a href="https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/apache-hadoop-introduction" target="_blank"><span style="color: #0066cc;" color="#0066cc">Apache Hadoop</span></a>, <a href="https://docs.microsoft.com/en-us/azure/hdinsight/kafka/apache-kafka-introduction" target="_blank"><span style="color: #0066cc;" color="#0066cc">Apache Kafka</span></a>, <a href="https://docs.microsoft.com/en-us/azure/hdinsight/hbase/apache-hbase-overview" target="_blank"><span style="color: #0066cc;" color="#0066cc">Apache HBase</span></a>, <a href="https://docs.microsoft.com/en-us/azure/hdinsight/storm/apache-storm-overview" target="_blank"><span style="color: #0066cc;" color="#0066cc">Apache Storm</span></a>, <a href="https://docs.microsoft.com/en-us/azure/hdinsight/r-server/r-server-overview" target="_blank"><span style="color: #0066cc;" color="#0066cc">Machine Learning Services</span></a>. HDInsight also supports a broad range of scenarios such as extraction, transformation, and loading (ETL); data warehousing; machine learning; and IoT. See <a href="https://azure.microsoft.com/en-us/services/hdinsight/" target="_blank"><span style="color: #0066cc;" color="#0066cc">HDInsight</span></a> for more general details.




### **Azure Data Lake Analytics**

<p style="text-align:left;"><img src="../Linked_Image_Files/datalakeanalytics.png" width="100" height="100" alt="Image representing Azure Data Lake Analytics"></p>

*Azure Data Lake Analytics* is an on-demand analytics job service that simplifies big data. Instead of deploying, configuring, and tuning hardware, you write queries to transform your data and extract valuable insights. The analytics service can handle jobs of any scale instantly by setting the dial for how much power you need. You only pay for your job when it is running, making it more cost-effective. See <a href="https://azure.microsoft.com/en-us/services/data-lake-analytics/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Data Lake Analytics</span></a>for more details.




**Note**: For a full list of big data and analytics services available with Azure, see the page <a href="https://azure.microsoft.com/en-us/product-categories/analytics/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Analytics</span></a>.