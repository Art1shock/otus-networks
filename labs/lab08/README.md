- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20S1.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20S2.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20R1.md)

# Лабораторная работа. Конфигурация безопасности коммутатора.

[Часть 1. ]()

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_1.png)

## Часть 1. Настройка основного сетевого устройства
### Шаг 1. Создайте сеть.
**a.	Создайте сеть согласно топологии.
b.	Инициализация устройств**

### Шаг 2. Настройте маршрутизатор R1.
**a.	Загрузите следующий конфигурационный скрипт на R1.
enable
configure terminal
hostname R1
no ip domain lookup
ip dhcp excluded-address 192.168.10.1 192.168.10.9
ip dhcp excluded-address 192.168.10.201 192.168.10.202
!
ip dhcp pool Students
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 domain-name CCNA2.Lab-11.6.1
!
interface Loopback0
 ip address 10.10.1.1 255.255.255.0
!
interface GigabitEthernet0/0/1
 description Link to S1
 ip dhcp relay information trusted
 ip address 192.168.10.1 255.255.255.0
 no shutdown
!
line con 0
 logging synchronous
 exec-timeout 0 0**
 
 ![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_2.png)
 
**b.	Проверьте текущую конфигурацию на R1, используя следующую команду:
R1# show ip interface brief**
**c.	Убедитесь, что IP-адресация и интерфейсы находятся в состоянии up / up (при необходимости устраните неполадки).**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_3.png)


[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab08)
