# Final Year Project Notes

## Ryu Setup with Open vSwitch
``` sudo mn --mac --switch ovsk --controller remote -x ```
Sets up mininet to listen to remote controller, topology is not specified in this command but could be


```
sudo su
ovs-vsctl set Bridge s1 protocols=OpenFlow13
ovs-vsctl set-manager ptcp:6632
``` 
This should be done on each switch changing s1 for s2, s3 etc.

Then start Ryu

Once Ryu is started, set listen port of OVSDB-server in controller

``` 
curl -X PUT -d '"tcp:127.0.0.1:6632"' http://localhost:8080/v1.0/conf/switches/0000000000000001/ovsdb_addr
```
