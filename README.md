# Spark-Projects
Repo to work on my Apache Spark skills and knowledge.


## About Spark
**Apache spark** is an open source framework intended to facilitate the handleing af large amount of data over a cluster. It is a modernisation of the **MapReduce** procedure created by Google. Spark Core, which handles the dirstibution of object(s) over the cluster can be acceses by using many diffferent apies i.e. PySpark for using Pyhton.


The cluster usually has a master node and some worker nodes. Optionally, you can have a history server that shows the data about completed applications. Completed applications are basically jobs that you submitted to Spark. And in terms of PySpark, this can be a Python script (_From: https://medium.com/@MarinAgli1/setting-up-a-spark-standalone-cluster-on-docker-in-layman-terms-8cbdc9fdd14b_).

### Benefits and disadvantages of Spark


```diff
Pros:
+ Speed when working with larger amounts of data
+ Flexibility in term of programming language
+ Near real-time data processing

Cons:
- High memory usage
- Small files problem
- Hard learning curve when used itermediate/advanced
- Not capable of genuine real-time processing
```

<!-- For '''diff reference:
+ text in green
- text in red
! text in orange
# text in gray
@@ text in purple (and bold)@@
-->


Resilient Distributed Dataset (RDD)

Directed Acyclic Graph (DAG)
