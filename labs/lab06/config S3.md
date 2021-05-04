- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab06)

Building configuration...  
  
Current configuration : 1593 bytes  
!  
version 15.0  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
service password-encryption  
!  
hostname S3  
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
 switchport mode trunk  
!  
interface FastEthernet0/2  
 switchport mode trunk  
!  
interface FastEthernet0/3  
 switchport mode trunk  
!  
interface FastEthernet0/4  
 switchport mode trunk  
!  
interface FastEthernet0/5  
 shutdown  
!  
interface FastEthernet0/6  
 shutdown  
!  
interface FastEthernet0/7  
 shutdown  
!  
interface FastEthernet0/8  
 shutdown  
!  
interface FastEthernet0/9  
 shutdown  
!  
interface FastEthernet0/10  
 shutdown  
!  
interface FastEthernet0/11  
 shutdown  
!  
interface FastEthernet0/12  
 shutdown  
!  
interface FastEthernet0/13  
 shutdown  
!  
interface FastEthernet0/14  
 shutdown  
!  
interface FastEthernet0/15  
 shutdown  
!  
interface FastEthernet0/16  
 shutdown  
!  
interface FastEthernet0/17  
 shutdown  
!  
interface FastEthernet0/18  
 shutdown  
!  
interface FastEthernet0/19  
 shutdown  
!  
interface FastEthernet0/20  
 shutdown  
!  
interface FastEthernet0/21  
 shutdown  
!  
interface FastEthernet0/22  
 shutdown  
!  
interface FastEthernet0/23  
 shutdown  
!  
interface FastEthernet0/24  
 shutdown  
!  
interface GigabitEthernet0/1  
!  
interface GigabitEthernet0/2  
!  
interface Vlan1  
 ip address 192.168.1.3 255.255.255.0  
!  
banner motd ^C  
For authorized users only   
^C  
!  
!  
!  
line con 0  
 password 7 0822455D0A16  
 logging synchronous  
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
