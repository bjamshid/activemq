# Steps to install mqtt thin client:

documentation can be found here:
 mqtt publisher: https://mosquitto.org/man/mosquitto_pub-1.html
 mqtt subscriber: https://mosquitto.org/man/mosquitto_sub-1.html

## 0. Update your machine and install the clients libraries:

sudo apt update && upgrade -y

sudo apt install mosquitto-clients

## 1. Check if everything works:

mosquitto_sub -h <your_broker_ip> -t test_topic

### in another terminal:
mosquitto_pub -h <your_broker_ip> -t test_topic -m "hello there"

## note: if you are running the broker in a VM and your thin clients out of VM, open/forward port 1883.
