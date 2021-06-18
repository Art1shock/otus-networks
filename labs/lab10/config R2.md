- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

Building configuration...  
  
Current configuration : 1045 bytes  
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
username SSHadmin privilege 15 secret 5 $1$mERr$jnsDknF4Wwkgx2tzKw49w1  
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
ip domain-name ccna-lab.com  
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
 ip address 10.20.0.4 255.255.255.0  
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
ip route 0.0.0.0 0.0.0.0 10.20.0.1   
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
 transport input ssh  
line vty 5 15  
 password 7 0822455D0A16  
 login  
!  
!  
!  
end  
