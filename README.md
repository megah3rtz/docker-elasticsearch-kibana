#docker-elasticsearch-kibana
This is an elasticsearch cluster (1 Master and 3 Slaves) with a kibana node connected to it.

To start the cluster.
'''
docker swarm init
docker stack deploy -c docker-compose.yml elasticstack
'''

Elasticsearch master is exposed on port 9200, and kibana on 5601.

To check the health of the elasticsearch cluster :
'''
curl -XGET 'localhost:9200/_cluster/health?pretty=true'
'''
To get started with kibana:
'''
http://localhost:5601
'''
