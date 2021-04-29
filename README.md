# NaOSA_Final-task
## Итоговая работа. Вариант №152
1. В качестве практической базы использовать `Cisco Packet Tracer`.
2. В зависимости от варианта задания реализовать сетевую топологию, состоящую из 6 маршрутизаторов типа `2911` (либо `Generic Router PT`, если необходим роутер с четырьмя сетевыми интерфейсами).
3. Задать адреса сетевым интерфейсам роутеров из таблицы, согласно варианта задания.
4. Настроить маршрутизацию между сетями:
   * *Четный вариант – статическая маршрутизация*.
   * Нечетный вариант - динамическая маршрутизация по протоколу RIP.
Все узлы, в том числе и роутеры, должны быть доступны.
5. К двум наиболее удаленным по топологии маршрутизаторам подключить:
   * к первому - компьютер `Server РТ`. Назначить статические адреса серверу и интерфейсу маршрутизатора из диапазона `192.168.Х.0/24`, где `Х` – номер варианта.
   * к второму - коммутатор `2960`.
6. На маршрутизаторе, к которому подключен `Server`, настроить статический NAT. В качестве глобального (белого) адреса взять адрес, который не является адресом интерфейса в этой сети.
7. На коммутаторе организовать три виртуальные локальные сети `VLAN 1` (vlan по умолчанию), `VLAN 2` и `VLAN 3`. В `VLAN2` включить беспроводной роутер `Linksys-WRT300N` и настроить его:
   * в качестве `SSID` использовать собственную фамилию на латинице;
   * в качестве пароля свое имя на латинице;
   * в качестве режима безопасности выбрать `WPA2-Personal`;
   * включить автоматическое определение каналов.
   
   К беспроводному роутеру подключить три беспроводных устройства. Для назначения адресов узлам беспроводной сети на беспроводном роутере настроить DHCP-сервер. Адреса выбрать из диапазона `192.168.Х.0/24`, где `Х` – номер варианта.
   На одном из беспроводных устройств (сервере) настроить сервис HTTP. На беспроводном роутере настроить перенаправление (проброс) портов, для доступа к HTTP-серверу беспроводной сети из любого узла внешней сети.
8. В `VLAN 3` включить два проводных устройства. Настроить транковый канал между коммутатором и роутером. На роутере настроить подинтерфейсы для всех `VLAN`. Для адресации подинтерфейсов использовать диапазон `192.168.Y.0/24`, где `Y = 255 - X`, а `X` – номер варианта, разбив его на необходимое число равных подсетей.
9. На любом из маршрутизаторов, кроме к которому подключен коммутатор, настроить DHCP-сервер, который будет раздавать адреса узлам в `VLAN 3`. На промежуточных роутерах настроить ретрансляцию `DHCP`.
10. На `Server'e`, в зависимости от варианта, настроить службы из таблицы:

    | Последняя цифра номера варианта | Сервис          |
    | ------------------------------- | --------------- |
    | *0, 1, 2*                       | MAIL, FTP, DNS  |
    | 3, 4, 5, 6                      | HTTP, MAIL, DNS |
    | 7, 8, 9                         | HTTP, FTP, DNS  |

    Проверить работоспособность сети и поддержку сервисов в любой точке объединенной сети.
11. На соответствующем маршрутизаторе настроить расширенный список доступа, который запретит для устройств проводной сети доступ по одному из протоколов, согласно варианта задания.

    | Последняя цифра номера варианта | Сервис |
    | ------------------------------- | ------ |
    | *0, 1, 2*                       | FTP    |
    | 3, 4, 5, 6                      | MAIL   |
    | 7, 8, 9                         | HTTP   |

*Курсивом выделены пункты моего варианта.*
