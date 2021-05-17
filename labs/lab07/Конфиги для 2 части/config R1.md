- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab07)

Building configuration...  
  
Current configuration : 1790 bytes  
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
ip dhcp excluded-address 192.168.1.65 192.168.1.69  
ip dhcp excluded-address 192.168.1.193 192.168.1.196  
ip dhcp excluded-address 192.168.1.129 192.168.1.133  
!  
ip dhcp pool VLAN200  
 network 192.168.1.192 255.255.255.224  
 default-router 192.168.1.193  
 domain-name CCNA-lab.com  
ip dhcp pool VLAN100  
 network 192.168.1.64 255.255.255.192  
 default-router 192.168.1.65  
 domain-name CCNA-lab.com  
ip dhcp pool R2_Client_Lan  
 network 192.168.1.128 255.255.255.240  
 default-router 192.168.1.129  
 domain-name CCNA-lab.com  
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
 ip address 10.0.0.1 255.255.255.252  
 duplex auto  
 speed auto  
!  
interface GigabitEthernet0/0/1  
 no ip address  
 duplex auto  
 speed auto  
!  
interface GigabitEthernet0/0/1.100  
 description Default Gateway for VLAN 100  
 encapsulation dot1Q 100  
 ip address 192.168.1.65 255.255.255.192  
!  
interface GigabitEthernet0/0/1.200  
 description Default Gateway for VLAN 200  
 encapsulation dot1Q 200  
 ip address 192.168.1.193 255.255.255.224  
!  
interface GigabitEthernet0/0/1.1000  
 description Default Gateway for VLAN 1000  
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
!  
ip classless  
ip route 192.168.1.128 255.255.255.240 10.0.0.2   
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
