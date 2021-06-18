- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/config%20S1.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/config%20S2.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/config%20R1.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/config%20R2.md)

# Лабораторная работа. Настройка и проверка расширенных списков контроля доступа.

[Часть 1. Создание сети и настройка основных параметров устройства](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-1-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B5%D1%82%D0%B8-%D0%B8-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D1%85-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D0%BE%D0%B2-%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0)  
[Часть 2. Настройка сетей VLAN на коммутаторах](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D1%81%D0%B5%D1%82%D0%B5%D0%B9-vlan-%D0%BD%D0%B0-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0%D1%85-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 3. Настройте транки (магистральные каналы)](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-3-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%82%D0%B5-%D1%82%D1%80%D0%B0%D0%BD%D0%BA%D0%B8-%D0%BC%D0%B0%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB%D1%8B-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 4. Настройте маршрутизацию](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-4-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%82%D0%B5-%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8E-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 5. Настройте удаленный доступ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-5-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%82%D0%B5-%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9-%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 6. Проверка подключения](https://github.com/Art1shock/otus-networks/blob/main/labs/lab10/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-6-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 7. Настройка и проверка списков контроля доступа (ACL)](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10#%D1%87%D0%B0%D1%81%D1%82%D1%8C-7-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%B8-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0-%D1%81%D0%BF%D0%B8%D1%81%D0%BA%D0%BE%D0%B2-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8F-%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0-acl-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_1.png)

## Часть 1. Создание сети и настройка основных параметров устройства

### Шаг 1. Создайте сеть согласно топологии.
**Подключите устройства, как показано в топологии, и подсоедините необходимые кабели.**

### Шаг 2. Произведите базовую настройку маршрутизаторов.
**a.	Назначьте маршрутизатору имя устройства.  
b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.  
f.	Зашифруйте открытые пароли.  
g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_2.png)

### Шаг 3. Настройте базовые параметры каждого коммутатора.
**a.	Присвойте коммутатору имя устройства.  
b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.  
f.	Зашифруйте открытые пароли.  
g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_3.png)

## Часть 2. Настройка сетей VLAN на коммутаторах [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

### Шаг 1. Создайте сети VLAN на коммутаторах.
#### a.	Создайте необходимые VLAN и назовите их на каждом коммутаторе из приведенной выше таблицы.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_4.png)

#### b.	Настройте интерфейс управления и шлюз по умолчанию на каждом коммутаторе, используя информацию об IP-адресе в таблице адресации. 

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_5.png)

#### c.	Назначьте все неиспользуемые порты коммутатора VLAN Parking Lot, настройте их для статического режима доступа и административно деактивируйте их.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_6.png)

### Шаг 2. Назначьте сети VLAN соответствующим интерфейсам коммутатора.

#### a.	Назначьте используемые порты соответствующей VLAN (указанной в таблице VLAN выше) и настройте их для режима статического доступа.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_7.png)

#### b.	Выполните команду show vlan brief, чтобы убедиться, что сети VLAN назначены правильным интерфейсам.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_8.png)

## Часть 3. Настройте транки (магистральные каналы) [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

### Шаг 1. Вручную настройте магистральный интерфейс F0/1.
#### a.	Измените режим порта коммутатора на интерфейсе F0/1, чтобы принудительно создать магистральную связь. Не забудьте сделать это на обоих коммутаторах.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_9.png)

**b.	В рамках конфигурации транка установите для native vlan значение 1000 на обоих коммутаторах. При настройке двух интерфейсов для разных собственных VLAN сообщения об ошибках могут отображаться временно.  
c.	В качестве другой части конфигурации транка укажите, что VLAN 20, 30, 40 и 1000 разрешены в транке.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_10.png)

#### d.	Выполните команду show interfaces trunk для проверки портов магистрали, собственной VLAN и разрешенных VLAN через магистраль.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_11.png)

### Шаг 2. Вручную настройте магистральный интерфейс F0/5 на коммутаторе S1.
**a.	Настройте интерфейс S1 F0/5 с теми же параметрами транка, что и F0/1. Это транк до маршрутизатора.  
b.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_12.png)

#### c.	Используйте команду show interfaces trunk для проверки настроек транка.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_13.png)

## Часть 4. Настройте маршрутизацию [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

### Шаг 1. Настройка маршрутизации между сетями VLAN на R1.
**a.	Активируйте интерфейс G0/0/1 на маршрутизаторе.  
b.	Настройте подинтерфейсы для каждой VLAN, как указано в таблице IP-адресации. Все подинтерфейсы используют инкапсуляцию 802.1Q. Убедитесь, что подинтерфейс для собственной VLAN не имеет назначенного IP-адреса. Включите описание для каждого подинтерфейса.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_14.png)

#### c.	Настройте интерфейс Loopback 1 на R1 с адресацией из приведенной выше таблицы.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_15.png)

#### d.	С помощью команды show ip interface brief проверьте конфигурацию подынтерфейса.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_16.png)

### Шаг 2. Настройка интерфейса R2 g0/0/1 с использованием адреса из таблицы и маршрута по умолчанию с адресом следующего перехода 10.20.0.1

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_17.1.png)

## Часть 5. Настройте удаленный доступ [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)

### Шаг 1. Настройте все сетевые устройства для базовой поддержки SSH.
**a.	Создайте локального пользователя с именем пользователя SSHadmin и зашифрованным паролем $cisco123!  
b.	Используйте ccna-lab.com в качестве доменного имени.  
c.	Генерируйте криптоключи с помощью 1024 битного модуля.  
d.	Настройте первые пять линий VTY на каждом устройстве, чтобы поддерживать только SSH-соединения и с локальной аутентификацией.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_18.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_19.png)

### Шаг 2. Включите защищенные веб-службы с проверкой подлинности на R1.
**a.	Включите сервер HTTPS на R1.  
R1(config)# ip http secure-server  
b.	Настройте R1 для проверки подлинности пользователей, пытающихся подключиться к веб-серверу.  
R1(config)# ip http authentication local**

Пакет трейсер не увидел такие команды (маршрутизатор самый последний 4331).

## Часть 6. Проверка подключения [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)
### Шаг 1. Настройте узлы ПК.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_20.png)

Шаг 2. Выполните следующие тесты. Эхозапрос должен пройти успешно.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_21.png)

Для PC-A:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_22.png)

Для PC-B:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_23.png)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_24.png)

Как видно все эхо-запросы прошли успешно.

## Часть 7. Настройка и проверка списков контроля доступа (ACL) [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)
#### При проверке базового подключения компания требует реализации следующих политик безопасности:
#### - Политика 1. Сеть Sales не может использовать SSH в сети Management (но в  другие сети SSH разрешен).  
#### - Политика 2. Сеть Sales не имеет доступа к IP-адресам в сети Management с помощью любого веб-протокола (HTTP/HTTPS). Сеть Sales также не имеет доступа к интерфейсам R1 с помощью любого веб-протокола. Разрешён весь другой веб-трафик (обратите внимание — Сеть Sales  может получить доступ к интерфейсу Loopback 1 на R1).  
#### - Политика 3. Сеть Sales не может отправлять эхо-запросы ICMP в сети Operations или Management. Разрешены эхо-запросы ICMP к другим адресатам.  
#### - Политика 4. Cеть Operations  не может отправлять ICMP эхозапросы в сеть Sales. Разрешены эхо-запросы ICMP к другим адресатам.

### Шаг 1. Проанализируйте требования к сети и политике безопасности для планирования реализации ACL.

Так как я не смог включить https сервер из-за того, что packet tracer не увидел нужные команды, то настрою списки ACL без учета второй политики. Вначале прописываю все политики в блокноте:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_25.png)

### Шаг 2. Разработка и применение расширенных списков доступа, которые будут соответствовать требованиям политики безопасности.

Теперь применяю все политики в packet tracer:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_26.png)

### Шаг 3. Убедитесь, что политики безопасности применяются развернутыми списками доступа.
Выполните следующие тесты. Ожидаемые результаты показаны в таблице:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_11/Screenshot_27.png)

[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab10)
