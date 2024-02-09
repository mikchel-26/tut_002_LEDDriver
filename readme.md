# Требования к  LED-драйверу:

1. LED-драйвер управляет 16-ю светодиодами с двумя состояниями.
2. Драйвер может включать и выключать отдельно любой светодиод  без затрагивания других.
3. Драйвер может включить и выключить все светодиоды с помощью одного вызова из интерфеса.
4. Пользователь драйвера может запросить состояние любого светодиода.
5. По умолчанию при включении питания светодиоды фиксируются. Светодиоды должны отключаться программно.
6. Светодиоды отображаются в памяти в 16-битное слово (по адресу, который необходимо определить).
7. 1 в позиции бита зажигает соответствующий светодиод; 0 выключает его.
8. Младший бит соответствует светодиоду 1; старший бит соответствует светодиоду 16.

> 1. The LED driver controls 16 two-state LEDs.
> 2. The driver can turn on or off any individual LED without affecting the others.
> 3. The driver can turn all LEDs on or off with a single interface call.
> 4. The user of the driver can query the state of any LED.
> 5. At power-on, the hardware default is for LEDs to be latched on. They must be turned off by the software.
> 6. LEDs are memory-mapped to a 16-bit word (at an address to be
determined).
> 7. A 1 in a bit position lights the corresponding LED; 0 turns it off.
> 8. The least significant bit corresponds to LED 1; the most significant bit corresponds to LED 16.

### Какие тесты нам нужны

* Все светодиоды погаснут после инициализации драйвера.
* Можно включить один светодиод.
* Один светодиод можно отключить.
* Несколько светодиодов можно включать/выключать.
* Включите все светодиоды
* Выключите все светодиоды
* Запрос состояния светодиода
* Проверьте граничные значения
* Проверьте значения за пределами границ