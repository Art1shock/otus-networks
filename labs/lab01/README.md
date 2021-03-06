- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab01/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)
- [СКАЧАТЬ ГОТОВУЮ СХЕМУ ДЛЯ CISCO PACKET TRACER](https://github.com/Art1shock/images/raw/main/%D0%94%D0%97_2.pkt)
# Лабораторная работа. Просмотр таблицы MAC-адресов коммутатора.

[Часть 1. Создание и настройка сети](https://github.com/Art1shock/otus-networks/blob/main/labs/lab01/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-1-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D1%81%D0%B5%D1%82%D0%B8-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 2. Изучение таблицы МАС-адресов коммутатора](https://github.com/Art1shock/otus-networks/blob/main/labs/lab01/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D0%B8%D0%B7%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B-%D0%BC%D0%B0%D1%81-%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%BE%D0%B2-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_23.png)

## Часть 1. Создание и настройка сети [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab01)
### Шаг 1. Подключите сеть в соответствии с топологией.

Создаю сеть согласно топологии:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.png)

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

## Часть 2. Изучение таблицы МАС-адресов коммутатора [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab01)

### Шаг 1. Запишите МАС-адреса сетевых устройств.

**a.	Откройте командную строку на PC-A и PC-B и введите команду ipconfig /all.**
**Введя данную команду на каждом из компьютеров можно назвать нужные MAC-адреса.**
**Назовите физические адреса адаптера Ethernet.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_14.png)

MAC-адрес компьютера PC-A: 0010.1180.DD23

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_15.png)

MAC-адрес компьютера PC-B: 0004.9A38.E0E3

**b.	Подключитесь к коммутаторам S1 и S2 через консоль и введите команду show interface F0/1 на каждом коммутаторе.**
**Назовите адреса оборудования во второй строке выходных данных команды (или зашитый адрес — bia).**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_16.png)

МАС-адрес коммутатора S1 Fast Ethernet 0/1: 0060.5cd1.4101

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_17.png)

МАС-адрес коммутатора S2 Fast Ethernet 0/1: 000a.f388.5401

### Шаг 2. Просмотрите таблицу МАС-адресов коммутатора.
**Подключитесь к коммутатору S2 через консоль и просмотрите таблицу МАС-адресов до и после тестирования сетевой связи с помощью эхо-запросов.**

**a.Подключитесь к коммутатору S2 через консоль и войдите в привилегированный режим EXEC.**

**b. В привилегированном режиме EXEC введите команду show mac address-table и нажмите клавишу ввода.
S2# show mac address-table**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_18.png)

**Записаны ли в таблице МАС-адресов какие-либо МАС-адреса?**

Записан один MAC-адрес.

**Какие МАС-адреса записаны в таблице? С какими портами коммутатора они сопоставлены и каким устройствам принадлежат? Игнорируйте МАС-адреса, сопоставленные с центральным процессором.**

Записан MAC-адрес порта FastEthernet 0/1 коммутатора S1.

**Если вы не записали МАС-адреса сетевых устройств в шаге 1, как можно определить, каким устройствам принадлежат МАС-адреса, используя только выходные данные команды show mac address-table? Работает ли это решение в любой ситуации?**

С помощью данной команды не получится.

### Шаг 3. Очистите таблицу МАС-адресов коммутатора S2 и снова отобразите таблицу МАС-адресов.
**a. В привилегированном режиме EXEC введите команду clear mac address-table dynamic и нажмите клавишу Enter.
S2# clear mac address-table dynamic**

**b. Снова быстро введите команду show mac address-table.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_19.png)

**Указаны ли в таблице МАС-адресов адреса для VLAN 1? Указаны ли другие МАС-адреса?**

Никаких MAC-адресов не указано.

**Через 10 секунд введите команду show mac address-table и нажмите клавишу ввода. Появились ли в таблице МАС-адресов новые адреса?**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_18.png)

Никаких новых адресов не появилось. Показан MAC-адрес порта FastEthernet 0/1 коммутатора S1, но его можно было увидеть и раньше, так что он не является новым.

### Шаг 4. С компьютера PC-B отправьте эхо-запросы устройствам в сети и просмотрите таблицу МАС-адресов коммутатора.

**a. На компьютере PC-B откройте командную строку и введите команду arp -a.
Не считая адресов многоадресной и широковещательной рассылки, сколько пар IP- и МАС-адресов устройств было получено через протокол ARP?**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_20.png)

Никаких адресов не появилось.

**b. Из командной строки PC-B отправьте эхо-запросы на компьютер PC-A, а также коммутаторы S1 и S2.
От всех ли устройств получены ответы? Если нет, проверьте кабели и IP-конфигурации.**

От всех устройств был получен ответ.

**c. Подключившись через консоль к коммутатору S2, введите команду show mac address-table.**
**Добавил ли коммутатор в таблицу МАС-адресов дополнительные МАС-адреса? Если да, то какие адреса и устройства?**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_21.png)

Появились три новых пары адресов (1, 2 и 4 строка). 

Соотнесение строк к устройствам:

1 строка - компьютер PC-B. 

2 строка - компьютер PC-A. 

4 строка - интерфейс VLAN 1 коммутатора S1.

**На компьютере PC-B откройте командную строку и еще раз введите команду arp -a.
Появились ли в ARP-кэше компьютера PC-B дополнительные записи для всех сетевых устройств, которым были отправлены эхо-запросы?**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_2/Screenshot_22.png)

Появилось 3 новых IP-адреса. Указаны все адреса, кроме одного - компьютера PC-B, с которого отправлялись эхо-запросы.

[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab01)
