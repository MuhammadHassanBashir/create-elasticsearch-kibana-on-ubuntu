# create-elasticsearch-kibana-on-ubuntu

## create-elasticsearch/kibana-on-ubuntu by using docker container

### Step for elastic search installation:

    1- docker network create elastic
    2- docker pull docker.elastic.co/elasticsearch/elasticsearch:8.6.1
    3- docker run --name elasticsearch --net elastic -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -t docker.elastic.co/elasticsearch/elasticsearch:8.6.1
    
### Step for kibana search installation:
    
    1- docker pull docker.elastic.co/kibana/kibana:8.6.1
    2- docker run --name kibana --net elastic -p 5601:5601 docker.elastic.co/kibana/kibana:8.6.1
