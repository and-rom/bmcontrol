BMcontrol
=========

Программа контроля и управления управляющим устройством MP707 для Linux-систем. 

BMcontrol позволяет передавать основные команды на управляющее устройство MP707, сканировать подключенные датчики температуры и получать от них данные. Программа реализована на С++ и работает из-под командной строки. Для работы программы необходима установленная в системе библиотека libusb-0.1.x.

Тестирование работоспособности проводилось на системах Debian Lenny и Mandriva 2010 spring. Вероятно будет работать и на других версиях Linux. Для пользователей Windows на [сайте разработчика](http://usbsergdev.narod.ru/BM1707/BM1707.html) всегда можно найти последнюю версию программы для вашей ОС.

Основные команды:
* **info** - отображает информацию о версии прошивки, серии USB и идентификатора.
* **scan** - сканирует и выводит найденные датчики температуры
* **temp \<id\>** - отображает температуру указанного в id температурного датчика
* **ports** - оторажает состояние портов управления
* **pset \<port\> \<status\>** - позволяет включать/выключать порты. Для значения port корректные значения 1 и 2, для значения status 0 - выкл, 1 - вкл.
* **psave** - сохраняет текущее состояние портов в память устройства. При следующем подключении устройства состояние портов будет автоматически восстановлено.
* **delay** - Отображает время неактивного состояние устройства, после которого устройство автоматически выключается.
* **delay \<5-255\>** - Задает время неактивного состояния устройства. Для версии прошивки 1h время может быть задано в пределах 5-255, для прошивки 2h значение может быть задано в 0, при этом функция отключения устройства не работает.


Исходники программы: [http://devphp.org.ua/bm.rar](http://devphp.org.ua/bm.rar)  
Версия для OpenWRT: [https://github.com/bubbafix/openwrt-bm1707](https://github.com/bubbafix/openwrt-bm1707)  
Версия 1.1: [https://code.google.com/p/bmcontrol/](https://code.google.com/p/bmcontrol/)  
Скомпилированная версия 1.1: [32-bit](http://devphp.org.ua/bmcontrol1.1_exec.tar.bz2) [64-bit](http://devphp.org.ua/bmcontrol1.1_64exec.tar.bz2)  

Скомпилированные версии:  
[1.0 32-bit](https://github.com/and-rom/bmcontrol/raw/master/bin/bmcontrol_x32_1.0)  
[1.1 32-bit](https://github.com/and-rom/bmcontrol/raw/master/bin/bmcontrol_x32_1.1)  
[1.1 64-bit](https://github.com/and-rom/bmcontrol/raw/master/bin/bmcontrol_x64_1.1)  
[1.1 64-bit альтернативная](https://github.com/and-rom/bmcontrol/raw/master/bin/bmcontrol_x64_1.1_alt)  
