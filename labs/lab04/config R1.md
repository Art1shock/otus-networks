- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab04)

Building configuration...  
  
Current configuration : 998 bytes  
!  
version 16.6.4  
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
no ip cef  
no ipv6 cef  
!  
!  
!  
username admin privilege 15 secret 5 $1$mERr$qJb.eHvBN7S590aq.dpRL.  
!  
!  
!  
!  
!  
!  
!  
!  
ip ssh version 2  
no ip domain-lookup  
ip domain-name domain.local  
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
 shutdown  
!  
interface GigabitEthernet0/0/1  
 ip address 192.168.1.1 255.255.255.0  
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
 login local  
line vty 5 15  
 password 7 0822455D0A16  
 login local  
!  
!  
!  
end  
