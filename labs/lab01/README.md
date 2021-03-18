# Лабораторная работа. Просмотр таблицы MAC-адресов коммутатора.
## Часть 1. Создание и настройка сети.
### Шаг 1. Подключите сеть в соответствии с топологией.

Создаю сеть согласно топологии:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0%20%D1%81%D0%B5%D1%82%D0%B8.png)

### Шаг 2. Настройте узлы ПК.

Задаю IP-адреса двум хостам (PC-A и PC-B):

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_1.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_2.png)

### Шаг 3. Выполните инициализацию и перезагрузку коммутаторов.

Перезагружаю коммутаторы с помощью комады **reload**. Как это выглядит для первого коммутатора:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_3.png)

### Шаг 4. Настройте базовые параметры каждого коммутатора.

**a. Настройте имена устройств в соответствии с топологией.**

Задаю имена коммутаторов в соответствии с топологией (S1 и S2):

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_4.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_5.png)

**b. Настройте IP-адреса, как указано в таблице адресации.**

Далее прописываю IP-адреса для VLAN 1 в каждом коммутаторе в соответствии с топологией:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_6.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_7.png)

**c. Назначьте cisco в качестве паролей консоли и VTY.**

Для S1:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_8.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_9.png)

Для S2:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_10.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_11.png)

**d. Назначьте class в качестве пароля доступа к привилегированному режиму EXEC.**

Для S1:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_12.png)

Для S2:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_13.png)

## Часть 2. Изучение таблицы МАС-адресов коммутатора.

### Шаг 1. Запишите МАС-адреса сетевых устройств.

**a.	Откройте командную строку на PC-A и PC-B и введите команду ipconfig /all.

Введя данную команду на каждом из компьютеров можно назвать нужные MAC-адреса.

Назовите физические адреса адаптера Ethernet.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_14.png)

MAC-адрес компьютера PC-A: FE::210:11FF:FE80:DD23

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_15.png)

MAC-адрес компьютера PC-B: FE80::204:9AFF:FE38:E0E3

**b.	Подключитесь к коммутаторам S1 и S2 через консоль и введите команду show interface F0/1 на каждом коммутаторе.

Назовите адреса оборудования во второй строке выходных данных команды (или зашитый адрес — bia).
МАС-адрес коммутатора S1 Fast Ethernet 0/1:
МАС-адрес коммутатора S2 Fast Ethernet 0/1:
