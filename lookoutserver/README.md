服务端默认会连接到 localhost:9200 的 ES 实例, 而我所用的开发机器是 MacOS，无法使用 --net=host 模式启动容器，因此在容器内无法通过 localhost:9200 连接 ES，需要使用如下方式绕过去：

```

gateway.metrics.exporter.es.host=es
metrics-server.spring.data.jest.uri=http://es:9200

```
