- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20S1.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20S2.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/config%20R1.md)

# Лабораторная работа. Конфигурация безопасности коммутатора.

[Часть 1. Настройка основного сетевого устройства](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-1-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%82%D0%B5%D0%B2%D0%BE%D0%B3%D0%BE-%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0)  
[Часть 2. Настройка сетей VLAN на коммутаторах](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D1%81%D0%B5%D1%82%D0%B5%D0%B9-vlan-%D0%BD%D0%B0-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0%D1%85)  
[Часть 3. Настройки безопасности коммутатора](https://github.com/Art1shock/otus-networks/blob/main/labs/lab08/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-3-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8-%D0%B1%D0%B5%D0%B7%D0%BE%D0%BF%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%D0%B8-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0)

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

### Шаг 3. Настройка и проверка основных параметров коммутатора
**a.	Настройте имя хоста для коммутаторов S1 и S2.
b.	Запретите нежелательный поиск в DNS.
c.	Настройте описания интерфейса для портов, которые используются в S1 и S2.
d.	Установите для шлюза по умолчанию для VLAN управления значение 192.168.10.1 на обоих коммутаторах.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_4.png)

## Часть 2. Настройка сетей VLAN на коммутаторах.
### Шаг 1. Сконфигруриуйте VLAN 10.
#### Добавьте VLAN 10 на S1 и S2 и назовите VLAN - Management.
### Шаг 2. Сконфигруриуйте SVI для VLAN 10.
#### Настройте IP-адрес в соответствии с таблицей адресации для SVI для VLAN 10 на S1 и S2. Включите интерфейсы SVI и предоставьте описание для интерфейса.
### Шаг 3. Настройте VLAN 333 с именем Native на S1 и S2.
### Шаг 4. Настройте VLAN 999 с именем ParkingLot на S1 и S2.

Выполнение всех 4-х шагов можно увидеть ниже:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_5.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_6.png)

## Часть 3. Настройки безопасности коммутатора.
### Шаг 1. Релизация магистральных соединений 802.1Q.
**a.	Настройте все магистральные порты Fa0/1 на обоих коммутаторах для использования VLAN 333 в качестве native VLAN.  
b.	Убедитесь, что режим транкинга успешно настроен на всех коммутаторах.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_7.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_8.png)

#### c.	Отключить согласование DTP F0/1 на S1 и S2. 

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_9.png)

#### d.	Проверьте с помощью команды show interfaces.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_10.png)

### Шаг 2. Настройка портов доступа
**a.	На S1 настройте F0/5 и F0/6 в качестве портов доступа и свяжите их с VLAN 10.  
b.	На S2 настройте порт доступа Fa0/18 и свяжите его с VLAN 10.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_11.png)

### Шаг 3. Безопасность неиспользуемых портов коммутатора
**a.	На S1 и S2 переместите неиспользуемые порты из VLAN 1 в VLAN 999 и отключите неиспользуемые порты.  
b.	Убедитесь, что неиспользуемые порты отключены и связаны с VLAN 999, введя команду  show.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_12.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_13.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_14.png)


### Шаг 4. Документирование и реализация функций безопасности порта.
**Интерфейсы F0/6 на S1 и F0/18 на S2 настроены как порты доступа. На этом шаге вы также настроите безопасность портов на этих двух портах доступа.  
a.	На S1, введите команду show port-security interface f0/6  для отображения настроек по умолчанию безопасности порта для интерфейса F0/6. Запишите свои ответы ниже.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_15.png)

**b.	На S1 включите защиту порта на F0 / 6 со следующими настройками:
o	Максимальное количество записей MAC-адресов: 3  
o	Режим безопасности: restrict  
o	Aging time: 60 мин.  
o	Aging type: неактивный**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_16.png)

**c.	Verify port security on S1 F0/6.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_9/Screenshot_17.png)


[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab08)
