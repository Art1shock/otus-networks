- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)

Building configuration...  
  
Current configuration : 1316 bytes  
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
 shutdown  
!  
interface GigabitEthernet0/0/1  
 no ip address  
 duplex auto  
 speed auto  
!  
interface GigabitEthernet0/0/1.10  
 description Default Gateway for VLAN 10  
 encapsulation dot1Q 10  
 ip address 192.168.10.1 255.255.255.0  
!  
interface GigabitEthernet0/0/1.20  
 description Default Gateway for VLAN 20  
 encapsulation dot1Q 20  
 ip address 192.168.20.1 255.255.255.0  
!  
interface GigabitEthernet0/0/1.30  
 description Default Gateway for VLAN 30  
 encapsulation dot1Q 30  
 ip address 192.168.30.1 255.255.255.0  
!  
interface GigabitEthernet0/0/1.1000  
 no ip address  
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
 login  
line vty 5 15  
 password 7 0822455D0A16  
 login  
!  
!  
!  
end  
