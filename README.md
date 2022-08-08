# openstack
Some roles and playbooks for use in Openstack

## IPv6
To create a dualstack network, a router and two VMs with the network attached  
```
$ ansible-playbook main.yml
```
**Note:** Default **ip6_ra_mode** and **ip6_address** mode are **'slaac'**
          Other values:  
          **IPv6 DHCP Stateful**: ipv_ra_mode:'dhcpv6-stateful', ipv6_address_mode:'dhcpv6-stateful'  
          **IPv6 DHCP Stateless**: ipv_ra_mode:'dhcpv6-stateless', ipv6_address_mode:'dhcpv6-stateless'  
          
To remove the resources creae by this scenario:  
```
$ ansible-playbook main.yaml -e create=false -e clean=true
```
