Было разработано
мобильное приложение – Ruby VPN. Это мобильное приложение под
Android которое позволяет безопасно и зашифровано подключаться к
интернету через удаленный сервер.

              Проектирование взаимодействия класfсов
Классы:
 Server - представляет собой класс, содержащий информацию о
сервере VPN, такую как IP-адрес, порт, имя сервера и другую
конфигурационную информацию.
 ServerList - класс для хранения списка серверов VPN. Он
позволяет добавлять, удалять и получать информацию о серверах.
 DBHelper - класс для управления базой данных SQLite,
используемой для хранения списка серверов VPN.
 VPNManager - класс для управления подключением к серверу
VPN и шифрованием данных. Он использует библиотеку OpenVPN для
установки соединения и шифрования данных.
 MainActivity - основной класс приложения, который отображает
список серверов VPN и позволяет пользователю подключаться к
выбранному серверу.
 ServerListAdapter - адаптер для списка серверов VPN, который
отображает информацию о серверах в пользовательском интерфейсе.

               Взаимодействие классов:
 MainActivity получает список серверов VPN из ServerList и
передает его в ServerListAdapter.
 Пользователь выбирает сервер из списка в ServerListAdapter и
нажимает кнопку "Подключиться".
 VPNManager использует информацию о выбранном сервере,
полученную от ServerList, для установки соединения и шифрования
данных.
 DBHelper используется для хранения и управления списком
серверов VPN в базе данных SQLite.
 При установлении соединения с сервером VPN, VPNManager
передает информацию о подключении обратно в MainActivity для
отображения соответствующего сообщения.
 Если приложение закрывается, DBHelper сохраняет текущий
список серверов VPN в базе данных, чтобы при следующем запуске
приложения можно было восстановить список серверов.

https://github.com/WooBears/VpnApp/assets/48993497/3b53b8d2-9ece-42e1-aabf-eb203d55600e
