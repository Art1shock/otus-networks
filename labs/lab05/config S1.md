- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)

Building configuration...  
  
Current configuration : 3191 bytes  
!  
version 15.0  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
service password-encryption  
!  
hostname S1  
!  
enable secret 5 $1$mERr$9cTjUIEqNGurQiFU.ZeCi1  
!  
!  
!  
no ip domain-lookup  
!  
!  
!  
spanning-tree mode pvst  
spanning-tree extend system-id  
!  
interface FastEthernet0/1  
 switchport trunk native vlan 1000  
 switchport trunk allowed vlan 10,20,30,1000  
 switchport mode trunk  
!  
interface FastEthernet0/2  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/3  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/4  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/5  
 switchport trunk native vlan 1000  
 switchport trunk allowed vlan 10,20,30,1000  
 switchport mode trunk  
!  
interface FastEthernet0/6  
 switchport access vlan 20  
 switchport mode access  
!  
interface FastEthernet0/7  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/8  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/9  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/10  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/11  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/12  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/13  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/14  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/15  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/16  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/17  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/18  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/19  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/20  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/21  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/22  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/23  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface FastEthernet0/24  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface GigabitEthernet0/1  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface GigabitEthernet0/2  
 switchport access vlan 999  
 switchport mode access  
 shutdown  
!  
interface Vlan1  
 no ip address  
 shutdown  
!  
interface Vlan10  
 ip address 192.168.10.11 255.255.255.0  
!  
interface Vlan20  
 no ip address  
!  
interface Vlan30  
 no ip address  
!  
interface Vlan999  
 no ip address  
 shutdown  
!  
interface Vlan1000  
 no ip address  
!  
ip default-gateway 192.168.10.1  
!  
banner motd ^C  
For authorized users only ^C  
!  
!  
!  
line con 0  
 password 7 0822455D0A16  
 login  
!  
line vty 0 4  
 password 7 0822455D0A16  
 login  
line vty 5 15  
 password 7 0822455D0A16  
 login  
!  
!  
!  
!  
end  
