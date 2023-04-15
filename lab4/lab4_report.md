> University: [ITMO University](https://itmo.ru/ru/)<br/>
> Faculty: [FICT](https://fict.itmo.ru)<br/>
> Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)<br/>
> Year: 2022/2023<br/>
> Group: K34202<br/>
> Author: Anisova Tatiana Sergeevna<br/>
> Lab: Lab4<br/>
> Date of create: 15.04.2023<br/>
> Date of finished: <br/>
# Описание
Построение сети IP-телефонии между удаленными маршрутизаторами.

# Цель работы
Изучить построение сети IP-телефонии между удаленными филиалами с помощью маршрутизаторов Cisco 2811 и коммутаторов Cisco 2950Т.

# Ход работы
## Часть 1
В начале работы в среде Cisco Packet Tracer была создана сеть следующего вида:

![Снимок экрана 2023-04-15 023643](https://user-images.githubusercontent.com/58114563/232173480-cd41f4ce-d93c-4f0a-b646-387f3fbbdd1d.png)

Чтобы обеспечить DCE-соединение между маршрутизаторами, потребовалось добавить на них разъемы:

![Снимок экрана 2023-04-15 023537](https://user-images.githubusercontent.com/58114563/232173545-3272dff5-6d35-4ad3-bd1c-7627f9c7e60a.png)

Затем на маршрутизаторах был настроен интерфейс FastEthernet:

![Снимок экрана 2023-04-15 025501](https://user-images.githubusercontent.com/58114563/232173669-e583e7e6-0e6d-4830-851d-5914d3263bbe.png)

![Снимок экрана 2023-04-15 025438](https://user-images.githubusercontent.com/58114563/232173672-7b9d7eed-bc76-426c-a972-b24652ad9c48.png)

После этого был сконфигурирован интерфейс Serial:

![Снимок экрана 2023-04-15 025525](https://user-images.githubusercontent.com/58114563/232173684-b1f88153-ec99-4f7d-a06b-d82309b5bb65.png)

![Снимок экрана 2023-04-15 025550](https://user-images.githubusercontent.com/58114563/232173689-c089c007-9c67-4a3c-8666-84ad182a44cb.png)

Далее на маршрутизаторах был настроен DHCP, создан пул адресов, включена опция 150 для работы CallManager Express:

![Снимок экрана 2023-04-15 025253](https://user-images.githubusercontent.com/58114563/232173742-8ac1a335-1260-4cf5-aec5-0ef2bc235496.png)

Также была настроена динамическая маршрутизация на основе протокола RIP.

После этого по аналогии с предыдущими работами был настроен телефонный сервис. Телефонам назначены номера 1101, 1102, 1103 в сети 192.168.0.0 и 1201, 1202, 1203 в сети 172.16.0.0.

Наконец, была настроена передача голоса между маршрутизаторами:

![Снимок экрана 2023-04-15 031018](https://user-images.githubusercontent.com/58114563/232173942-1d4080be-3f35-427b-8e65-f11acdd5112f.png)

После всех этих действий телефонная связь была проверена:

![image](https://user-images.githubusercontent.com/58114563/232174019-8d6abfb5-d856-49b1-b4f9-72b108cf2684.png)

Также была проверена IP-связность компьютеров:

![image](https://user-images.githubusercontent.com/58114563/232174042-203cc6a5-d739-4519-aed1-d21905119e29.png)

## Вывод
В ходе выполнения лабораторной работы была построена сеть IP-телефонии между удаленными филиалами.
