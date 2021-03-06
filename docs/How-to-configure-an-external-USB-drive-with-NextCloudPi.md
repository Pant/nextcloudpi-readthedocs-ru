# ru_How-to-configure-an-external-USB-drive-with-NextCloudPi.html


## Выберите интерфейс пользователя
Вы можете настроить NextCloudPi экземпляр из терминального пользовательского интерфейса (TUI) или из веб-интерфейса (WebUI).
Внимание: *Бэкенд остаётся тот же.*  Все параметры доступны в любом пользовательском интерфейсе.

### TUI (Терминальный пользовательский интерфейс)

Чтобы получить доступ к терминалу, надо сперва включить SSH на вашем Raspberry Pi. Подробнее смотрите [здесь](https://github.com/nextcloud/nextcloudpi/wiki/How-to-install-NextCloudPi-on-a-Raspberry-Pi#first-steps). 

Альтернативно, вы можете подключить клавиатуру и экран HDMI для доступа к терминалу.

![](https://camo.githubusercontent.com/4b2c6bbb044a6bd59a01582017fa91ab85e023a5/68747470733a2f2f6f776e796f7572626974732e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031372f30332f6e63702d636f6e662d373030783435362e6a7067)

#### Raspberry Pi
1.Подключите клавиатуру и экран HDMI.
2.Включите ваш Raspberry Pi с образом для SD-карты NextCloudPi.
3.Войдите в систему, пользователь 'pi' а пароль 'raspberry'.
4.(Необязательно) введите 'sudo raspi-config' и включите SSH в "Параметры взаимодействия".
5.(Необязательно) введите 'sudo nextcloudpi-config' и используйте ['nc-wifi'][nc-wifi] для подключения к вашему WLAN. (вашей беспроводной локальной сети)

#### Linux / Mac
1.Откройте терминал.
2.Подключитесь к своему Raspberry Pi с 'ssh'. Вы можете использовать команду 'ssh pi@"localIPAdress"'. "LocalIPAdress"(без кавычек) является локальным IP-адресом Pi.
3.Введите пароль 'raspberry'.


#### Windows
1.Установите Putty с [этого веб-сайта](http://www.putty.org/)
2.Запустите Putty и напишите IP-адрес вашего Raspberry Pi в поле "Host Name". 
3.Выберите "SSH" из кнопок "Тип соединения". Номер порта изменится на "22".
4.Нажмите "Открыть" в правом нижнем углу.
5.Введите пароль 'raspberry'.

Вы теперь подключились к оболочке NextCloudPi. Запуская команду 'nextcloudpi-config' вы можете открыть TUI.

### WebUI
Если вы теперь хотите настроить NextCloudPi с помощью WebUI:
1.Откройте ваш веб-браузер.
2.Напишите в URL-адресе "https: //« raspberryPiAddress »: 4443". Замените "raspberryPiAddress"(без кавычек) на IP-адрес вашего Raspberry Pi.
3.Вам должно появиться сообщение о том, что IP-адрес который вы посещаете не является безопасным. Вам следует  принять самоподписанный сертификат. Вы можете нажать на кнопку 'Дополнительно' которая находится на странице предупреждения. Потом нажмите на кнопку 'Добавить исключение', как показано на нижнем изображение:
![Accept Signed NCP certificate.](https://user-images.githubusercontent.com/14947634/34748770-10015646-f596-11e7-8f56-4e33cf5c9260.png)
Всё это происходит потому, что по умолчанию браузеры не распознают самоподписанные сертификаты. 
4.Вам будет предложено ввести один пароль. На старых установках вы можете использовать пользователь 'pi' и пароль 'raspberry'. На новых установках всё это изменилось. Пользователь теперь 'ncp' а пароль 'ownyourbits'. После начальной настройки, вы должны изменить этот пароль используя диалог 'nc-passwd'.

После этого вы увидите веб-панель:

![](https://ownyourbits.com/wp-content/uploads/2017/09/ncp-web-demo.gif)

---

Отсюда вы можете настроить всё что вы хотите. Посмотрите [Ссылка на Конфигурацию](https://github.com/nextcloud/nextcloudpi/wiki/Configuration-Reference) . Тут есть объяснения для всех параметров.

Выполните следующие шаги чтобы получить [доступ извне](https://github.com/nextcloud/nextcloudpi/wiki/How-to-access-from-outside-your-network).

Выполните следующие шаги чтобы [разместить свои данные на USB-флешке](https://github.com/nextcloud/nextcloudpi/wiki/How-to-configure-an-external-USB-drive-with-NextCloudPi).

Вы можете прочитать [это руководство](https://ownyourbits.com/2017/12/30/sync-nextcloud-tasks-calendars-and-contacts-on-your-android-device/)](https://ownyourbits.com/2017/12/30/sync-nextcloud-tasks-calendars-and-contacts-on-your-android-device/) если вы хотите синхронизировать ваши файлы, контакты, задачи и календари NextCloudPi с вашим Android телефоном .