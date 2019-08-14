# steps to register activemq as a service daemon -- not tested

## 0. copy and save the content of 'activemq' to here:
  sudo nano /etc/init.d/activemq

## 1. change access permissions
  sudo chmod +x /etc/init.d/activemq

## maybe required:
	sudo chown root:root /etc/init.d/activemq

## 2. register the daemon as a service:
	sudo update-rc.d activemq defaults

## 3. restart the service:
	sudo service activemq restart

## 4. check service status
  service activemq status

## 5. Stopping the service
  service activemq stop
