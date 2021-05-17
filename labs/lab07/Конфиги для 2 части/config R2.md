- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab07)

Building configuration...  
  
Current configuration : 1074 bytes  
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
ipv6 unicast-routing  
!  
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
interface GigabitEthernet0/0/0  
 no ip address  
 duplex auto  
 speed auto  
 ipv6 address FE80::2 link-local  
 ipv6 address 2001:DB8:ACAD:2::2/64  
!  
interface GigabitEthernet0/0/1  
 no ip address  
 duplex auto  
 speed auto  
 ipv6 address FE80::1 link-local  
 ipv6 address 2001:DB8:ACAD:3::1/64  
 ipv6 nd managed-config-flag  
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
ipv6 route 2001:DB8:ACAD:1::/64 2001:DB8:ACAD:2::1  
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
