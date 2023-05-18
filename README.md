### Docker compose to run a env for using kafka.

to start use the command: <br/>
`docker-compose up -d`
<br/><br/>

to access the kafka's container: <br/>
`docker-compose exec kafka bash`
<br/><br/>

to clean the console use:<br/>
`ctrl+l`
<br/><br/>

to create a topic:<br/>
`kafka-topics --create --topic=topic_name --boostrap-server=localhost:9092 --partitions=3`
<br/><br/>

to list every topic (it's mandatory to pass the bootstrap-server):<br/>
`kafka-topics --list --bootstrap-server=localhost:9092`
<br/><br/>

to create a consumer (it's mandatory to pass the bootstrap-server):<br/>
`kafka-console-consumer --bootstrap-server=localhost:9092 --topic=topic_name`
<br/><br/>

to create a producer (execute in a different terminal):<br/>
`kafka-console-producer --boostrap-server=localhost:9092 --topic=topic_name`
<br/>
- after the command every word you hit, it's going to show in the consumer