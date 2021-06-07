- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab09)

Building configuration...  
  
Current configuration : 1191 bytes  
!  
version 15.4  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
service password-encryption  
!  
hostname R2  
!  
!  
!  
enable secret 5 $1$mERr$9cTjUIEqNGurQiFU.ZeCi1  
!  
!  
!  
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
interface Loopback1  
 ip address 192.168.1.1 255.255.255.0  
 ip ospf network point-to-point  
 ip ospf priority 1  
 ip ospf 56 area 0  
!  
interface GigabitEthernet0/0/0  
 no ip address  
 duplex auto  
 speed auto  
 shutdown  
!  
interface GigabitEthernet0/0/1  
 ip address 10.53.0.2 255.255.255.0  
 ip ospf hello-interval 30  
 ip ospf dead-interval 120  
 ip ospf 56 area 0  
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
router ospf 56  
 router-id 2.2.2.2  
 log-adjacency-changes  
 passive-interface Loopback1  
 auto-cost reference-bandwidth 500  
!  
ip classless  
!  
ip flow-export version 9  
!  
!  
!  
banner motd ^C  
For authorized users only ^C  
!  
!  
!  
!  
!  
line con 0  
 password 7 0822455D0A16  
 login  
!  
line aux 0  
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
end  
