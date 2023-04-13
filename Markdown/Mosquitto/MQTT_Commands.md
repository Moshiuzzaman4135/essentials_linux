# Mosqitto
## Install moquitto client with the following command in linux
```
apt-get install mosquitto-clients
```
## Check if moquitto is installed with
```
mosquitto
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

