# Import to elasticserach

###RabbitMQ
1. To work with the RabbitMQ used library php-amqplib/rabbitmq-bundle
2. To add a task you should start provider
    * `./app/console app:provider  xml /your/directory/source-xml/`
    * `./app/console app:provider  json /your/directory/source-json/`
3. To perform a task you should start a consumer:
    * `./app/console rabbitmq:consumer  upload_tasks`

###ElasticSearch
1. To work with ElasticSearch used library elasticsearch/elasticsearch
2. There was created a service elasticsearch. It was injected into the upload_tasks_service(callback for a consumer).

###Structure
1. TaskConsumer:`src/AppBundle/Consumer/TaskConsumer.php`
2. TaskProducer:`src/AppBundle/Producer/TaskProducer.php`
3. ProviderCommand:`src/AppBundle/Command/ProviderCommand.php`
4. ProviderCommand:`src/AppBundle/Command/ProviderCommand.php`
5. ElasticSearch service:`src/AppBundle/ElasticSearch/ElasticSearch.php`
