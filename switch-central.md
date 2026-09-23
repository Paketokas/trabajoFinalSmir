Switch>enable
Switch#show running-config
Building configuration...

Current configuration : 1058 bytes
!
version 12.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
!
!
ptp clock transparent domain 0 profile default
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
 switchport access vlan 10
!
interface FastEthernet1/1
 switchport access vlan 10
!
interface FastEthernet2/1
 switchport access vlan 10
!
interface FastEthernet3/1
 switchport access vlan 10
!
interface FastEthernet4/1
 switchport access vlan 20
!
interface FastEthernet5/1
 switchport access vlan 20
!
interface FastEthernet6/1
 switchport access vlan 20
!
interface FastEthernet7/1
 switchport access vlan 20
!
interface FastEthernet8/1
 switchport access vlan 10
 switchport trunk allowed vlan 2-1005
 switchport mode access
!
interface FastEthernet9/1
 switchport access vlan 20
 switchport trunk allowed vlan 1-29,31-1001
 switchport mode access
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end
