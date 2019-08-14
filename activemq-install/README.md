# steps to install an Apache ActiveMQ

documentation can be found here: http://activemq.apache.org/

# 0. Install jdk:

sudo apt update && upgrade -y

sudo apt install default-jre -y

## optional: create a directory

mkdir broker-iot

cd broker-iot


# 1. Download Apache ActiveMQ:

wget https://www-eu.apache.org/dist/activemq/5.15.8/apache-activemq-5.15.8-bin.tar.gz

# 2. Extract the downloaded file, i.e., apache-activemq-x.yy.z-bin.tar.gz and then remove the compressed package:

tar zxvf apache-activemq-5.15.8-bin.tar.gz

sudo rm apache**-bin*

# 3. Navigate to bin folder in extracted directory:

cd apache-activemq-5.15.8/bin

# 4. Start activemq - you can start it either in daemon mode -in which you will find the logs in data/ directory - or in console mode:

./activemq console

## daemon mode

./activemq start

# 5. Check if everything works:

http://localhost:8161/admin

	user: admin

	pass: admin

# 6. Stopping activemq:

	# console mode: ctrl + c
	## in daemon mode: ./activemq stop

	# if none of the above works, open another terminal and execute the following:
ps -ef | grep 'activemq' | grep -v grep | awk '{print $2}' | xargs -r kill -9
