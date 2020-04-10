# elasticssearch-window10
elasticssearch 7.0.1 on Windows 10

Elasticssearch 7.0.1 does not work with jdk 1.13.  Because of size limit at github, this repo does not include bundled jdk in elasticssearch zip.

To run
1. download zip from https://www.elastic.co/guide/en/elasticsearch/reference/7.x/zip-windows.html, and unzip.
2. unset JAVA_HOME enviroment variable so elasticssearch uses bundled java in /jdk
3. bin\elasticsearch.bat

To check status:  URL http://localhost:9200/_cluster/health should return something like

{"cluster_name":"elasticsearch","status":"yellow","timed_out":false,"number_of_nodes":1,"number_of_data_nodes":1,"active_primary_shards":5,"active_shards":5,"relocating_shards":0,"initializing_shards":0,"unassigned_shards":5,"delayed_unassigned_shards":0,"number_of_pending_tasks":0,"number_of_in_flight_fetch":0,"task_max_waiting_in_queue_millis":0,"active_shards_percent_as_number":50.0}
