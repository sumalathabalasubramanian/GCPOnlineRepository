# GCPOnlineTransfer
Connect to GCS from Databricks Community cloud: 
https://docs.databricks.com/en/connect/storage/gcs.html

## Setup:
1. Create an All-Purpose compute cluster in Databricks with below Spark configs. 
   * spark.hadoop.fs.gs.auth.service.account.private.key.id xxxxxx 
   * spark.hadoop.fs.gs.auth.service.account.private.key xxxxxx 
   * spark.hadoop.google.cloud.auth.service.account.enable true 
   * spark.hadoop.fs.gs.project.id xxxxxx 
   * spark.hadoop.fs.gs.auth.service.account.email xxxxxx 
   * spark.databricks.rocksDB.fileManager.useCommitService false
2. Install gcs connector jar in libraries.
   * Import the connector jar in DBFS location and then install
   * Jar is available in gcs - gs://hadoop-lib/gcs/gcs-connector-hadoop2-2.2.7.jar
3. Create table default.studentrecords with sample records in Databricks tables.
4. Execute the python notebook file - Databricks_2_GCP.ipynb

