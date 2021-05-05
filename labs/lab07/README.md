- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ (СХЕМА СЕТИ ОБЩАЯ ДЛЯ ОБОИХ ЧАСТЕЙ)](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  

**Лабораторная работа разделена на 2 большие части:**
1) [Лабораторная работа. Реализация DHCPv4.](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/README.md#%D0%BB%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%80%D0%B5%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-dhcpv4)  
1.1 [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%201%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20S1.md)  
1.2 [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%201%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20S2.md)  
1.3 [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%201%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20R1.md)  
1.4 [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%201%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20R2.md)
2) [Лабораторная работа. Настройка DHCPv6.](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/README.md#%D0%BB%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-dhcpv6)  
2.1 [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%202%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20S1.md)  
2.2 [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%202%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20S2.md)  
2.3 [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%202%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20R1.md)  
2.4 [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab07/%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D0%B8%20%D0%B4%D0%BB%D1%8F%202%20%D1%87%D0%B0%D1%81%D1%82%D0%B8/config%20R2.md)

# Лабораторная работа. Реализация DHCPv4.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_8/%D0%A7%D0%B0%D1%81%D1%82%D1%8C_1/Screenshot_1.png)

## Часть 1. Создание сети и настройка основных параметров устройства
**В первой части лабораторной работы вам предстоит создать топологию сети и настроить базовые параметры для узлов ПК и коммутаторов.**
### Шаг 1. Создание схемы адресации
**Создать подсеть сети 192.168.1.0/24 в соответствии со следующими требованиями:
a.	Одна подсеть «Подсеть A», поддерживающая 58 хостов (клиентская VLAN на R1).**

Подсеть A:

**Запишите первый IP-адрес в таблице адресации для R1 G0/0/1.100. Запишите второй IP-адрес в таблице адресов для S1 VLAN 200 и введите соответствующий шлюз по умолчанию.**

**b.	Одна подсеть «Подсеть B», поддерживающая 28 хостов (управляющая VLAN на R1).**

Подсеть B:

**Запишите первый IP-адрес в таблице адресации для R1 G0/0/1.200. Запишите второй IP-адрес в таблице адресов для S1 VLAN 1 и введите соответствующий шлюз по умолчанию.**

**c.	Одна подсеть «Подсеть C», поддерживающая 12 узлов (клиентская сеть на R2).**

Подсеть C:

**Запишите первый IP-адрес в таблице адресации для R2 G0/0/1.**

В итоге получается следующая таблица адресации:

.......

# Лабораторная работа. Настройка DHCPv6. [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab07)

[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab07)
