- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/config%20S1.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/config%20S2.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/config%20R1.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/config%20R2.md)
- [СКАЧАТЬ ГОТОВУЮ СХЕМУ ДЛЯ CISCO PACKET TRACER](https://github.com/Art1shock/images/raw/main/%D0%94%D0%97_10.pkt)

# Лабораторная работа. Настройка протокола OSPFv2 для одной области.

[Часть 1. Создание сети и настройка основных параметров устройства](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-1-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B5%D1%82%D0%B8-%D0%B8-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D1%85-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D0%BE%D0%B2-%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0)  
[Часть 2. Настройка и проверка базовой работы протокола  OSPFv2 для одной области](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%B8-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D0%B1%D0%B0%D0%B7%D0%BE%D0%B2%D0%BE%D0%B9-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B-%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D0%B0-ospfv2-%D0%B4%D0%BB%D1%8F-%D0%BE%D0%B4%D0%BD%D0%BE%D0%B9-%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D0%B8-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 3. Оптимизация и проверка конфигурации OSPFv2 для одной области](https://github.com/Art1shock/otus-networks/blob/main/labs/lab09/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-3-%D0%BE%D0%BF%D1%82%D0%B8%D0%BC%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%B8-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D0%B8-ospfv2-%D0%B4%D0%BB%D1%8F-%D0%BE%D0%B4%D0%BD%D0%BE%D0%B9-%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D0%B8-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_1.png)

## Часть 1. Создание сети и настройка основных параметров устройства
### Шаг 1. Создайте сеть согласно топологии.
#### Подключите устройства, как показано в топологии, и подсоедините необходимые кабели.
### Шаг 2. Произведите базовую настройку маршрутизаторов.
**a.	Назначьте маршрутизатору имя устройства.  
b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.  
f.	Зашифруйте открытые пароли.  
g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_2.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_3.png)

### Шаг 3. Настройте базовые параметры каждого коммутатора.
**a.	Назначьте коммутатору имя устройства.  
b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.  
f.	Зашифруйте открытые пароли.  
g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_4.png)

## Часть 2. Настройка и проверка базовой работы протокола OSPFv2 для одной области [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab09)
### Шаг 1. Настройте адреса интерфейса и базового OSPFv2 на каждом маршрутизаторе.
#### a.	Настройте адреса интерфейсов на каждом маршрутизаторе, как показано в таблице адресации выше.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_5.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_7.png)

#### b.	Перейдите в режим конфигурации маршрутизатора OSPF, используя идентификатор процесса 56.
#### c.	Настройте статический идентификатор маршрутизатора для каждого маршрутизатора (1.1.1.1 для R1, 2.2.2.2 для R2).

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_6.png)

#### d.	Настройте инструкцию сети для сети между R1 и R2, поместив ее в область 0.
#### e.	Только на R2 добавьте конфигурацию, необходимую для объявления сети Loopback 1 в область OSPF 0.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_26.png)

#### f.	Убедитесь, что OSPFv2 работает между маршрутизаторами. Выполните команду, чтобы убедиться, что R1 и R2 сформировали смежность.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_29.png)

Маршрутизаторы видят друг друга, значит все настроено правильно.

#### Какой маршрутизатор является DR? Какой маршрутизатор является BDR? Каковы критерии отбора?

DR (Designated Router) - роутер R2, а BDR (Backup Designated Router) - роутер R1. Маршрутизаторы соединены в сети Ethernet, поэтому OSPF выбрал DR и BDR автоматически. В качестве DR был выбран роутер R2, так как у него самый высокий идентификатор - 2.2.2.2.

#### g.	На R1 выполните команду show ip route ospf, чтобы убедиться, что сеть R2 Loopback1 присутствует в таблице маршрутизации. Обратите внимание, что поведение OSPF по умолчанию заключается в объявлении интерфейса обратной связи в качестве маршрута узла с использованием 32-битной маски.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_11.png)

#### h.	Запустите Ping до  адреса интерфейса R2 Loopback 1 из R1. Выполнение команды ping должно быть успешным.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_12.png)

Пинг успешен.

## Часть 3. Оптимизация и проверка конфигурации OSPFv2 для одной области [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab09)
### Шаг 1. Реализация различных оптимизаций на каждом маршрутизаторе.
#### a.	На R1 настройте приоритет OSPF интерфейса G0/0/1 на 50, чтобы убедиться, что R1 является назначенным маршрутизатором.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_14.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_15.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_16.png)

Как видно, после изменения приоритета и перезапуска процесса OSPF маршрутизатор R1 теперь стал DR.

#### b.	Настройте таймеры OSPF на G0/0/1 каждого маршрутизатора для таймера приветствия, составляющего 30 секунд.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_17.png)

#### c.	На R1 настройте статический маршрут по умолчанию, который использует интерфейс Loopback 1 в качестве интерфейса выхода. Затем распространите маршрут по умолчанию в OSPF. Обратите внимание на сообщение консоли после установки маршрута по умолчанию.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_18.1.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_19.png)


#### d.	добавьте конфигурацию, необходимую для OSPF для обработки R2 Loopback 1 как сети точка-точка. Это приводит к тому, что OSPF объявляет Loopback 1 использует маску подсети интерфейса.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_25.png)

#### e.	Только на R2 добавьте конфигурацию, необходимую для предотвращения отправки объявлений OSPF в сеть Loopback 1.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_28.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_27.1.png)

#### f.	Измените базовую пропускную способность для маршрутизаторов. После этой настройки перезапустите OSPF с помощью команды clear ip ospf process. Обратите внимание на сообщение консоли после установки новой опорной полосы пропускания.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_20.2.png)

### Шаг 2. Убедитесь, что оптимизация OSPFv2 реализовалась.
#### a.	Выполните команду show ip ospf interface g0/0/1 на R1 и убедитесь, что приоритет интерфейса установлен равным 50, а временные интервалы — Hello 30, Dead 120, а тип сети по умолчанию — Broadcast

Дополнительно изменяю интервал Dead на 120:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_21.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_33.png)

Вывод команды **show ip ospf interface g0/0/1**:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_22.1.png)

#### b.	На R1 выполните команду show ip route ospf, чтобы убедиться, что сеть R2 Loopback1 присутствует в таблице маршрутизации. Обратите внимание на разницу в метрике между этим выходным и предыдущим выходным. Также обратите внимание, что маска теперь составляет 24 бита, в отличие от 32 битов, ранее объявленных.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_30.1.png)

#### c.	Введите команду show ip route ospf на маршрутизаторе R2. Единственная информация о маршруте OSPF должна быть распространяемый по умолчанию маршрут R1.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_31.png)

#### d.	Запустите Ping до адреса интерфейса R1 Loopback 1 из R2. Выполнение команды ping должно быть успешным.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_10/Screenshot_32.png)

#### Почему стоимость OSPF для маршрута по умолчанию отличается от стоимости OSPF в R1 для сети 192.168.1.0/24?



[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab09)
