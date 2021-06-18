- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

Building configuration...  
  
Current configuration : 2321 bytes  
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
interface Loopback1  
 ip address 172.16.1.1 255.255.255.0  
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
interface GigabitEthernet0/0/1.20  
 description Default Gateway for VLAN 20  
 encapsulation dot1Q 20  
 ip address 10.20.0.1 255.255.255.0  
!  
interface GigabitEthernet0/0/1.30  
 description Default Gateway for VLAN 30  
 encapsulation dot1Q 30  
 ip address 10.30.0.1 255.255.255.0  
 ip access-group 120 in  
!  
interface GigabitEthernet0/0/1.40  
 description Default Gateway for VLAN 40  
 encapsulation dot1Q 40  
 ip address 10.40.0.1 255.255.255.0  
 ip access-group 110 in  
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
access-list 110 deny tcp 10.40.0.0 0.0.0.255 10.20.0.0 0.0.0.255 eq 22  
access-list 110 permit tcp 10.40.0.0 0.0.0.255 10.30.0.0 0.0.0.255 eq 22  
access-list 110 permit tcp 10.40.0.0 0.0.0.255 10.40.0.0 0.0.0.255 eq 22  
access-list 110 permit tcp 10.40.0.0 0.0.0.255 172.16.1.0 0.0.0.255 eq 22  
access-list 110 deny icmp 10.40.0.0 0.0.0.255 10.20.0.0 0.0.0.255  
access-list 110 deny icmp 10.40.0.0 0.0.0.255 10.30.0.0 0.0.0.255  
access-list 110 permit icmp 10.40.0.0 0.0.0.255 10.40.0.0 0.0.0.255  
access-list 110 permit icmp 10.40.0.0 0.0.0.255 172.16.1.0 0.0.0.255  
access-list 120 deny icmp 10.30.0.0 0.0.0.255 10.40.0.0 0.0.0.255  
access-list 120 permit icmp 10.30.0.0 0.0.0.255 10.20.0.0 0.0.0.255  
access-list 120 permit icmp 10.30.0.0 0.0.0.255 10.30.0.0 0.0.0.255  
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
