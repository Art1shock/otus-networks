- [ВЕРНУТЬСЯ К СПИСКУ ЛАБОРАТОРНЫХ РАБОТ](https://github.com/Art1shock/otus-networks/tree/main/labs)  
- [ПОСМОТРЕТЬ СХЕМУ СЕТИ](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/%D0%A1%D1%85%D0%B5%D0%BC%D0%B0_%D1%81%D0%B5%D1%82%D0%B8.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/config%20S1.md)  
- [ПОСМОТРЕТЬ КОНФИГ КОММУТАТОРА S2](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/config%20S2.md)  
- [ПОСМОТРЕТЬ КОНФИГ МАРШРУТИЗАТОРА R1](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/config%20R1.md)
- [СКАЧАТЬ ГОТОВУЮ СХЕМУ ДЛЯ CISCO PACKET TRACER](https://github.com/Art1shock/images/raw/main/%D0%94%D0%97_6.pkt)

# Лабораторная работа. Внедрение маршрутизации между виртуальными локальными сетями.

[Часть 1. Создание сети и настройка основных параметров устройства](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-1-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B5%D1%82%D0%B8-%D0%B8-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D1%85-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D0%BE%D0%B2-%D1%83%D1%81%D1%82%D1%80%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 2. Создание сетей VLAN и назначение портов коммутатора](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-2-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B5%D1%82%D0%B5%D0%B9-vlan-%D0%B8-%D0%BD%D0%B0%D0%B7%D0%BD%D0%B0%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D1%80%D1%82%D0%BE%D0%B2-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 3. Конфигурация магистрального канала стандарта 802.1Q между коммутаторами](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-3-%D0%BA%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B0%D1%86%D0%B8%D1%8F-%D0%BC%D0%B0%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB%D0%B0-%D1%81%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82%D0%B0-8021q-%D0%BC%D0%B5%D0%B6%D0%B4%D1%83-%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0%D0%BC%D0%B8-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 4. Настройка маршрутизации между сетями VLAN](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/README.md#%D1%87%D0%B0%D1%81%D1%82%D1%8C-4-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8-%D0%BC%D0%B5%D0%B6%D0%B4%D1%83-%D1%81%D0%B5%D1%82%D1%8F%D0%BC%D0%B8-vlan-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BD%D0%B0%D0%B2%D0%B5%D1%80%D1%85)  
[Часть 5. Проверьте, работает ли маршрутизация между VLAN](https://github.com/Art1shock/otus-networks/blob/main/labs/lab05/README.md#%D1%87a%D1%81%D1%82%D1%8C-5-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D1%8C%D1%82%D0%B5-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%B5%D1%82-%D0%BB%D0%B8-%D0%BC%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%BC%D0%B5%D0%B6%D0%B4%D1%83-vlan-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BDa%D0%B2%D0%B5%D1%80%D1%85)

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_15.png)

## Часть 1. Создание сети и настройка основных параметров устройства [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
#### В первой части лабораторной работы вам предстоит создать топологию сети и настроить базовые параметры для узлов ПК и коммутаторов.

### Шаг 1. Создайте сеть согласно топологии.
#### Подключите устройства, как показано в топологии, и подсоедините необходимые кабели.

### Шаг 2. Настройте базовые параметры для маршрутизатора.
#### a.	Подключитесь к маршрутизатору с помощью консоли и активируйте привилегированный режим EXEC.  
#### b.	Войдите в режим конфигурации.  
#### c.	Назначьте маршрутизатору имя устройства.  

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_2.png)

#### d.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
#### e.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
#### f.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
#### g.	Установите cisco в качестве пароля виртуального терминала и активируйте вход.  
#### h.	Зашифруйте открытые пароли.  
#### i.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
#### j.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.  
#### k.	Настройте на маршрутизаторе время.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_3.png)

### Шаг 3. Настройте базовые параметры каждого коммутатора.
#### a.	Присвойте коммутатору имя устройства.  
#### b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.  
#### c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.  
#### d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.  
#### e.	Установите cisco в качестве пароля виртуального терминала и активируйте вход.  
#### f.	Зашифруйте открытые пароли.  
#### g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.  
#### h.	Настройте на коммутаторах время.  
#### i.	Сохранение текущей конфигурации в качестве начальной.

Для коммутатора S1:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_4.png)

Для коммутатора S2:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_5.png)

### Шаг 4. Настройте узлы ПК.

Для PC-A:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_6.png)

Для PC-B:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_7.png)

## Часть 2. Создание сетей VLAN и назначение портов коммутатора [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
**Во второй части вы создадите VLAN, как указано в таблице выше, на обоих коммутаторах. Затем вы назначите VLAN соответствующему интерфейсу и проверите настройки конфигурации. Выполните следующие задачи на каждом коммутаторе.**

### Шаг 1. Создайте сети VLAN на коммутаторах.
#### a.	Создайте и назовите необходимые VLAN на каждом коммутаторе из таблицы выше.  

Создаю VLAN 10 с именем administration для обоих коммутаторов:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_8.png)  
![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_9.png)

По аналогии создаю оставшиеся сети VLAN и получаю следующее:

Для коммутатора S1:

Для наглядности продемонстрирую как присвоить нужный интерфейс конкретной VLAN:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_10.png)

Далее создав оставшиеся VLAN получаю следующий итог:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_29.png)

Для коммутатора S2:

Так как ранее я продемонстрировал как присвоить интерфейс конкретной VLAN, то просто покажу все VLAN'ы через команду **show vlan brief**:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_30.png)

#### b.	Настройте интерфейс управления и шлюз по умолчанию на каждом коммутаторе, используя информацию об IP-адресе в таблице адресации.  

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_12.png)  
![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_31.png)

#### c.	Назначьте все неиспользуемые порты коммутатора VLAN Parking_Lot, настройте их для статического режима доступа и административно деактивируйте их.

Для коммутатора S1:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_29.png)

Для коммутатора S2:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_30.png)

### Шаг 2. Назначьте сети VLAN соответствующим интерфейсам коммутатора.
#### a.	Назначьте используемые порты соответствующей VLAN (указанной в таблице VLAN выше) и настройте их для режима статического доступа.
#### b.	Убедитесь, что VLAN назначены на правильные интерфейсы.

Все это было сделано. Вывод команды **show vlan brief** для каждого коммутатора был показан выше, все назначено в соответствии с таблицей.

## Часть 3. Конфигурация магистрального канала стандарта 802.1Q между коммутаторами [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
#### В части 3 вы вручную настроите интерфейс F0/1 как транк.

### Шаг 1. Вручную настройте магистральный интерфейс F0/1 на коммутаторах S1 и S2.
**a.	Настройка статического транкинга на интерфейсе F0/1 для обоих коммутаторов.  
b.	Установите native VLAN 1000 на обоих коммутаторах.  
c.	Укажите, что VLAN 10, 20, 30 и 1000 могут проходить по транку.**

Для S1:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_16.png)

Для S2:

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_17.png)

#### d.	Проверьте транки, native VLAN и разрешенные VLAN через транк.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_18.png)  
![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_19.png)

Все настроено правильно.

### Шаг 2. Вручную настройте магистральный интерфейс F0/5 на коммутаторе S1.
**a.	Настройте интерфейс S1 F0/5 с теми же параметрами транка, что и F0/1. Это транк до маршрутизатора.  
b.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.  
c.	Проверка транкинга.**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_20.png)  
![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_21.png)

#### Что произойдет, если G0/0/1 на R1 будет отключен?

Соедиенение f0/5 и g0/0/1 прервется.

## Часть 4. Настройка маршрутизации между сетями VLAN [ВЕРНУТЬСЯ НАВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
### Шаг 1. Настройте маршрутизатор.
**a.	При необходимости активируйте интерфейс G0/0/1 на маршрутизаторе.  
b.	Настройте подинтерфейсы для каждой VLAN, как указано в таблице IP-адресации. Все подинтерфейсы используют инкапсуляцию 802.1Q. Убедитесь, что подинтерфейсу для native VLAN   не назначен IP-адрес. Включите описание для каждого подинтерфейса.  
c.	Убедитесь, что вспомогательные интерфейсы работают**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_22.png)  
![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_23.png)

## Чaсть 5. Проверьте, работает ли маршрутизация между VLAN [ВЕРНУТЬСЯ НAВЕРХ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
### Шаг 1. Выполните следующие тесты с PC-A. Все должно быть успешно.
#### a.	Отправьте эхо-запрос с PC-A на шлюз по умолчанию.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_24.png)

Эхо-запрос успешен.

#### b.	Отправьте эхо-запрос с PC-A на PC-B.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_26.png)

Эхо-запрос успешен.

#### c.	Отправьте команду ping с компьютера PC-A на коммутатор S2.

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_27.png)

Эхо-запрос успешен.

**Шаг 2. Пройдите следующий тест с PC-B
В окне командной строки на PC-B выполните команду tracert на адрес PC-A.
Какие промежуточные IP-адреса отображаются в результатах?**

![](https://github.com/Art1shock/images/blob/main/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D0%94%D0%97_6/Screenshot_28.png)

Видно 2 адреса: адрес PC-B и адрес шлюза по умолчанию для VLAN 30.

[ВЕРНУТЬСЯ НАВЕРХ СТРАНИЦЫ](https://github.com/Art1shock/otus-networks/tree/main/labs/lab05)
