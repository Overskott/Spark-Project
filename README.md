# Spark-Projects

Collection of notes and projects regarding Apache Spark to be used as reference.


## About Spark
**Apache spark** is an open source framework intended to facilitate the handleing af large amount of data over a cluster. It is a modernisation of the **MapReduce** procedure created by Google. Spark Core, which handles the dirstibution of object(s) over the cluster can be acceses by using many diffferent apies i.e. PySpark for using Pyhton.


The cluster usually has a master node and some worker nodes. Optionally, you can have a history server that shows the data about completed applications. Completed applications are basically jobs that you submitted to Spark. And in terms of PySpark, this can be a Python script [^MarinAgli1].

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
(small files problem)[^Patil]

<!-- For '''diff reference:
+ text in green
- text in red
! text in orange
# text in gray
@@ text in purple (and bold)@@
-->

## Datatypes, Transformations and Actions

This paragraph is based on the introduction video [^Coder2j]

### Resilient Distributed Dataset (RDD)
- Backbone of data processing in Spark
- Distributed, fault-tolerant, and parallelizable data structure
- Efficiently processes large datasets across a cluster
- Key characteristics:
  - Immutable: Cannot modify a RDD. Transformations create new RDDs
  - Distributed: Data partitioned and processed in parallel
  - Resilient: Lineage tracks transformations for fault tolerance, allowing it to recover lost data and continue computation in case of failures
  - Lazily evaluated: Execution plan optimized, transformations evaluated when necessary
  - Fault-tolerant operations: map, filter, reduce, collect, count, save, etc.
 
- Transformations:
  - Create new RDDs by applying computation/maipulation
  - Lax\zy evaluations, lineage graph
  - Examples: map, filter, flatMap, reduceByKey, sortBy, join

- Actions:
  - Return restults or performing actions on RDD, trigger executions
  - Eagerly evaluated, data movement/computation
  - Examples: collect, count, first, take, save, foreach
    
### Dataframes
- Powerful abstraction for distributet and styructured data
- Similar structure to a relational database
- **Schema information:** Enables query optimization and various other optimizations

**Advantages of DataFrames over RDDs**
```diff
Optimized execution:
+ Schema information enables query optimization and predicate pushdowns
+ Faster and more efficient data processing
Ease of use:
+ High-level. SQL-like interface for data interaction
+ Simplified compared to complex RDD transformations
Integration with Ecosystem:
+ Seamless integration with Spark's ecosystem (Spark SQL, MLlib, GraphX)
+ Leverage various libraries and functinalities
Built-in optimization:
+ Leveraging Spark's Catalys optimizer for advanced optimization
+ Predicate pushdown, constant folding, loop unrolling
Interoperability:
+ Easily convert to/from other data formats (e.g. Pandas DataFrames)
+ Seamless interegation with other data processing tools
```


### Directed Acyclic Graph (DAG)

### Sources:

[^MarinAgli1]: https://medium.com/@MarinAgli1/setting-up-a-spark-standalone-cluster-on-docker-in-layman-terms-8cbdc9fdd14b

[^Coder2j]: (PySpark Tutorial for Beginners)[https://www.youtube.com/watch?v=EB8lfdxpirM]

[^Patil]: https://medium.com/globant/how-to-solve-a-large-number-of-small-files-problem-in-spark-21f819eb36d3
