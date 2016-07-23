### LogAnalysisDemo_real-time_dxc
- **Flume**(producer)监控日志文件，当日志文件中有新的数据时，通过agent source的exec方式，将数据push到**kafka**broker对应的topic上，等待数据被消费。
- **Spark streaming**(consumer)根据zookeeper上存储的元数据信息，从kafka broker上对应的partition那里pull数据，并结合**SparkSQL**进行数据的处理。
- 数据处理后，利用python的图形库**bokeh**(可显示增量数据)，将信息实时地显示在浏览器中


###目录说明
    Flume_kafka_dxc.ppt是flume和kafka的培训ppt(讲解他们的原理，使用等等)
    SparkStreaming_dxc .ppt是sparkstreaming的培训PPT(讲解sparkstreaming的原理，使用等等)
    app-20151111041944-0762-f26ff739   是demo使用到的日志数据
    demo_程序.txt  是相关的demo程序和指令
    日志分析配套文档.md  是整个说明文档
