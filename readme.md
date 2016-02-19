Elastic Stack Demo
==================

docker-machine create -d virtualbox elastic

docker-compose up

VBoxManage controlvm "elastic" natpf1 "es9200-port,tcp,,9200,,9200"
VBoxManage controlvm "elastic" natpf1 "es9300-port,tcp,,9300,,9300"
VBoxManage controlvm "elastic" natpf1 "kibana-port,tcp,,5601,,5601"
VBoxManage controlvm "elastic" natpf1 "logstash-http-port,tcp,,5000,,5000"