- [ВЕРНУТЬСЯ НАЗАД](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

Building configuration...  
  
Current configuration : 2953 bytes  
!  
version 15.0  
no service timestamps log datetime msec  
no service timestamps debug datetime msec  
service password-encryption  
!  
hostname S2  
!  
enable secret 5 $1$mERr$9cTjUIEqNGurQiFU.ZeCi1  
!  
!  
!  
ip ssh version 2  
no ip domain-lookup  
ip domain-name ccna-lab.com  
!  
username SSHadmin secret 5 $1$mERr$jnsDknF4Wwkgx2tzKw49w1  
!  
!  
!  
spanning-tree mode pvst  
spanning-tree extend system-id  
!  
interface FastEthernet0/1  
 switchport trunk native vlan 1000  
 switchport trunk allowed vlan 20,30,40,1000  
 switchport mode trunk  
!  
interface FastEthernet0/2  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/3  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/4  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/5  
 switchport access vlan 20  
 switchport mode access  
!  
interface FastEthernet0/6  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/7  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/8  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/9  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/10  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/11  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/12  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/13  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/14  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/15  
 switchport access vlan 999   
 switchport mode access  
!  
interface FastEthernet0/16  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/17  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/18  
 switchport access vlan 40  
 switchport mode access  
!  
interface FastEthernet0/19  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/20  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/21  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/22  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/23  
 switchport access vlan 999  
 switchport mode access  
!  
interface FastEthernet0/24  
 switchport access vlan 999  
 switchport mode access  
!  
interface GigabitEthernet0/1  
 switchport access vlan 999  
 switchport mode access  
!  
interface GigabitEthernet0/2  
 switchport access vlan 999  
 switchport mode access  
!  
interface Vlan1  
 no ip address  
 shutdown  
!  
interface Vlan20  
 ip address 10.20.0.3 255.255.255.0  
!  
interface Vlan30  
 no ip address  
!  
interface Vlan40  
 no ip address  
!  
ip default-gateway 10.20.0.1  
!  
banner motd ^C  
For authorized users only ^C  
!  
!  
!  
line con 0  
 password 7 0822455D0A16  
 login  
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
!  
end  
