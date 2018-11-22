# dataflow-wordcount-bigquery-edition

## 実行
ローカル
```
  mvn compile exec:java　-Dexec.mainClass=org.apache.beam.examples.WordCount -Dexec.args="--tempLocation=gs://<STORAGE_BUCKET>"
```


デプロイ
```
  mvn -Pdataflow-runner compile exec:java -Dexec.mainClass=org.apache.beam.examples.WordCount -Dexec.args="--project=<PROJECT_ID> --stagingLocation=gs://<STORAGE_BUCKET>/staging/ --runner=DataflowRunner --tempLocation=gs://<STORAGE_BUCKET>/temp"
```

## 参考

[公式](https://cloud.google.com/dataflow/docs/quickstarts/quickstart-java-maven?hl=ja)  

[beam.apache.org](https://beam.apache.org/releases/javadoc/2.1.0/org/apache/beam/sdk/io/gcp/bigquery/BigQueryIO.html)  

[github](https://github.com/GoogleCloudPlatform/training-data-analyst)
