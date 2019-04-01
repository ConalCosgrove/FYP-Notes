# Final Year Project Notes

## Ryu Setup with Open vSwitch
``` sudo mn --mac --switch ovsk --controller remote -x ```
Sets up mininet to listen to remote controller, topology is not specified in this command but could be


```sudo su``` 

```ovs-vsctl set Bridge s1 protocols=OpenFlow13``` 

