- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab08)

Building configuration...  
  
Current configuration : 1033 bytes  
!  
version 15.4  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
no service password-encryption  
!  
hostname R1  
!  
!  
!  
!  
ip dhcp excluded-address 192.168.10.1 192.168.10.9  
ip dhcp excluded-address 192.168.10.201 192.168.10.202  
!  
ip dhcp pool Students  
 network 192.168.10.0 255.255.255.0  
 default-router 192.168.10.1  
 domain-name CCNA2.Lab-11.6.1  
!  
!  
!  
ip cef  
no ipv6 cef  
!  
!  
!  
!  
!  
!  
!  
!  
!  
!  
no ip domain-lookup  
!  
!  
spanning-tree mode pvst  
!  
!  
!  
!  
!  
!  
interface Loopback0  
 ip address 10.10.1.1 255.255.255.0  
!  
interface GigabitEthernet0/0/0  
 no ip address  
 duplex auto  
 speed auto  
 shutdown  
!  
interface GigabitEthernet0/0/1  
 description Link to S1  
 ip address 192.168.10.1 255.255.255.0  
 duplex auto  
 speed auto  
!  
interface GigabitEthernet0/0/2  
 no ip address  
 duplex auto  
 speed auto  
 shutdown  
!  
interface Vlan1  
 no ip address  
 shutdown  
!  
ip classless  
!  
ip flow-export version 9  
!  
!  
!  
no cdp run  
!  
!  
!  
!  
!  
!  
line con 0  
 exec-timeout 0 0  
 logging synchronous  
!  
line aux 0  
!  
line vty 0 4  
 login  
!  
!  
!  
end  
