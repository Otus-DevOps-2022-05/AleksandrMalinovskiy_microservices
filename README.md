# AleksandrMalinovskiy_microservices\
AleksandrMalinovskiy microservices repository\
ДЗ docker-4\
Выполнено все согласно методичке.\
По итогу имеем запущеное приложение на ip:9292, но теперь запущенное и описаное в docker-compose.yml\
Самостоятельное задание:
- Изменить docker-compose под кейс с множеством сетей, сетевых алиасов (стр 18).
- Параметризуйте с помощью переменных окружений:
• порт публикации сервиса ui
• версии сервисов
• возможно что-либо еще на ваше усмотрение
- Параметризованные параметры запишите в отдельный файл c расширением .env
- Без использования команд source и export docker-compose должен подхватить переменные из этого файла.
- Узнайте как образуется базовое имя проекта. Можно ли его задать? Если можно то как? \
Сделано:\
Добавлен алиас к монге\
В docker-compose.yml указаны переменные описанные в .env при запуске docker-compose up -d берутся переменные из файла.\
В docker-compose.yml добалены строки container_name: для того что бы указать имя контейнера
_________
ДЗ docker -3\
Выполнено все согласно методичке.\
По истогу получили запущенное приложение в докере на ip:9292\
Для хранения информации вне докера подклбчили волиум к монге\
В ходе выполнения задания со * были уменьшены размеры image за счет оптимизации сборки\
________
ДЗ docker -1,2\
Выполнено все согласно методичке.\
В итоге приложение запущенное в докере на хосте ВМ в яндекс клауд\
Образ загружен в докер хаб
