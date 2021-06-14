# springboot-mqtt-poc

## Installing

 <https://mosquitto.org/download/> for details on installing binaries for various platforms.

## Quick start
NOTE : run mosquitto.exe on command prompt.

    mosquitto

Then use "mosquitto_sub" to subscribe to a topic:

    mosquitto_sub -t 'test/topic' -v

And to publish a message:

    mosquitto_pub -t 'test/topic' -m 'this is test message !!'
	


POST Method : 
http://localhost:8080/api/mqtt/publish

BODY : 
{
	"message": "this is test message !!",
	"topic":"test",
	"retained":true,
	"qos":1
}

GET Method : 
http://localhost:8080/api/mqtt/subscribe?topic=test&wait_millis=5000