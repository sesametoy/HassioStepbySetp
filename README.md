# HassioStepbySetp
install ubuntu and update
```
sudo apt-get update
sudo apt-get upgrade
sudo reboot
```

install core pack
```
sudo apt-get install  linux-image-extra-$(uname -r)  linux-image-extra-virtual
```
# install docker-ce

```
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common
```
install docker source
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

install docker-ce
```
sudo apt-get update
sudo apt-get install docker-ce
```
```
sudo systemctl enable docker
sudo systemctl start docker
```

# install other package
```
sudo apt-get install bash jq avahi-daemon dbus apparmor-utils network-manager
```
# install hassio
```
sudo su
curl -sL https://raw.githubusercontent.com/home-assistant/hassio-installer/master/hassio_install.sh | bash -s
```

Command line arguments
argument	default	description
-m | --machine		On a special platform they need set a machine type use
-d | --data-share	/usr/share/hassio	data folder for hass.io installation
you can set these parameters by appending -- <parameter> <value> like:
```
curl -sL https://raw.githubusercontent.com/home-assistant/hassio-installer/master/hassio_install.sh | bash -s -- -m MY_MACHINE
```
