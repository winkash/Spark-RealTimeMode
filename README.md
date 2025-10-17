# Spark-RealTimeMode
Real-time mode, a trigger type for Structured Streaming that enables ultra-low latency data processing with end-to-end latency as low as 5 ms. 

# Cluster configuration
To use real-time mode in Structured Streaming, you must configure a classic Lakeflow Job:
In your Databricks workspace, 
1. click New in the upper-left corner. Choose More and click Cluster.
2. Clear Photon acceleration.
3. Clear Enable autoscaling.
4. Under Advanced performance, clear Use spot instances.
5. Under Advanced and Access mode, click Manual and select Dedicated (formerly: Single user).
6. Under Spark, enter the following under Spark config:
   spark.databricks.streaming.realTimeMode.enabled true
7. Click Create

From Databricks Runtime 16.4 LTS and above, all real-time pipelines use checkpoint v2, which allows seamless switching between real-time and micro-batch modes.
