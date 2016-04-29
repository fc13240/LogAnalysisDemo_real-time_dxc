### LogAnalysisDemo_real-time_dxc
- **Flume**(producer)监控日志文件，当日志文件中有新的数据时，通过agent source的exec方式，将数据push到**kafka**broker对应的topic上，等待数据被消费。
- **Spark streaming**(consumer)根据zookeeper上存储的元数据信息，从kafka broker上对应的partition那里pull数据，并结合**SparkSQL**进行数据的处理。
- 数据处理后，利用python的图形库**bokeh**(可显示增量数据)，将信息实时地显示在浏览器中
