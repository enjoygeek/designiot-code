#Lan IoT

##HTTP 

GET请求:

```
curl http://localhost:3000/api
```

POST请求:

```
curl -X PUT -d '{ "led": true }' -H "Content-Type: application/json" http://localhost:3000/api/
```

PUT请求:

```
curl -X POST -d '{ "led": true }' -H "Content-Type: application/json" http://localhost:3000/api/
```

DELETE请求:

```
curl -X DELETE http://localhost:3000/api
```


POST Devices:

```
curl -X POST -d '{ "led": true,"temperature": 15 }' -H "Content-Type: application/json" http://localhost:3000/user/1/devices/1
```

##MQTT

publish

```
mosquitto_pub -t 'test/topic' -m 45 -q 1
```

subscribe

```
mosquitto_sub -v -t 'test/topic'
```

mqtt.js

```
mqtt sub -v -t 'device/2'
mqtt pub -t 'device/2' -m 35
```    