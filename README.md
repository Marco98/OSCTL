# OSCTL
OSCTL is a simple bash script that can be used to quickly restart all OpenStack services at once. It is easy to add, modify and remove service presets.

## Usage:
```
osctl {service|all|list} [start|stop|restart|status] remote
```
## Installation:
To install the script as intended just drop it in at **/usr/local/bin/**
```
sudo wget -O /usr/local/bin/osctl  https://raw.githubusercontent.com/Marco98/OpenStackCTL/master/osctl
sudo chmod +x /usr/local/bin/osctl
```
## Example:
```
osctl computectl restart 192.168.0.3
```
This will restart the following services:
* openstack-nova-api.service
* openstack-nova-consoleauth.service
* openstack-nova-scheduler.service
* openstack-nova-conductor.service
* openstack-nova-novncproxy.service

## Default Presets:
**computectl**
* openstack-nova-api.service
* openstack-nova-consoleauth.service
* openstack-nova-scheduler.service
* openstack-nova-conductor.service
* openstack-nova-novncproxy.service

**compute**
* libvirtd.service
* openstack-nova-compute.service

**blockstoragectl**
* openstack-cinder-api.service
* openstack-cinder-scheduler.service

**blockstorage**
* openstack-cinder-volume.service

**networking**
* neutron-server.service
* neutron-linuxbridge-agent.service
* neutron-dhcp-agent.service
* neutron-metadata-agent.service
* neutron-l3-agent.service
* neutron-linuxbridge-agent.service
	
**image**
* openstack-glance-api.service
* openstack-glance-registry.service
