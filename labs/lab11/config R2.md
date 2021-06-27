- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab11)

Building configuration...  
  
Current configuration : 1106 bytes  
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
 ip address 209.165.200.1 255.255.255.224  
!  
interface GigabitEthernet0/0/0  
 ip address 209.165.200.225 255.255.255.248  
 duplex auto  
 speed auto  
!  
interface GigabitEthernet0/0/1  
 no ip address  
 duplex auto  
 speed auto  
 shutdown  
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
ip route 192.168.1.0 255.255.255.0 209.165.200.230   
!  
ip flow-export version 9  
!  
!  
!  
banner motd ^C  
-----------------------------------------------  
---------For authorized users only-------------  
-----------------------------------------------  
^C  
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
