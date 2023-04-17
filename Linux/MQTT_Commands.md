# Mosqitto
## Install moquitto client with the following command in linux
```
apt-get install mosquitto-clients
```
## Check if moquitto is installed with
```
mosquitto
```
## Start mosquitto
```
sudo systemctl start mosquitto
```
## Status mosquitto
```
sudo systemctl status mosquitto
```
## Stop mosquitto
```
sudo service mosquitto stop
sudo systemctl stop mosquitto.service
```



### To publish in a topic with mosquitto with a file payload
```
mosquitto_pub -h 127.0.0.1 -u username -P password -i id@id.com -t /topic -f payload_file.json
```
### To publish in a topic with mosquitto with a message
```
mosquitto_pub -h 127.0.0.1 -t /topic -m 'Message'
```
### Subscribe to a topic
```
mosquitto_sub -h 127.0.0.1 -t /topic
```
### See mqtt connection summary for every second
```
watch -n1 "netstat -anl | grep 1883 | awk '/^tcp/ {t[\$NF]++} END{for(state in t){print state, t[state]} }'"
```

