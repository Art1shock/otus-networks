- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab07)

Building configuration...  
  
Current configuration : 1370 bytes  
!  
version 15.4  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
service password-encryption  
!  
hostname R1  
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
ipv6 dhcp pool R1-STATELESS  
 dns-server 2001:DB8:ACAD::254  
 domain-name STATELESS.com  
!  
ipv6 dhcp pool R2-STATEFUL  
 address prefix 2001:db8:acad:3:aaa::/80 lifetime 172800 86400  
 dns-server 2001:DB8:ACAD::254  
 domain-name STATEFUL.com  
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
 ipv6 address FE80::1 link-local  
 ipv6 address 2001:DB8:ACAD:2::1/64  
 ipv6 dhcp server R2-STATEFUL  
!  
interface GigabitEthernet0/0/1  
 no ip address  
 duplex auto  
 speed auto  
 ipv6 address FE80::1 link-local  
 ipv6 address 2001:DB8:ACAD:1::1/64  
 ipv6 nd other-config-flag  
 ipv6 dhcp server R1-STATELESS  
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
ipv6 route 2001:DB8:ACAD:3::/64 2001:DB8:ACAD:2::2  
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
