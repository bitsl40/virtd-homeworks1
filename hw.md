# Домашнее задание к занятию 5. «Практическое применение Docker»


---

## Задача 1
1. Сделайте в своем GitHub пространстве fork [репозитория](https://github.com/netology-code/shvirtd-example-python).

2. Создайте файл ```Dockerfile.python``` на основе существующего `Dockerfile`:
   - Используйте базовый образ ```python:3.12-slim```
   - Обязательно используйте конструкцию ```COPY . .``` в Dockerfile
   - Создайте `.dockerignore` файл для исключения ненужных файлов
   - Используйте ```CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "5000"]``` для запуска
   - Протестируйте корректность сборки 
3. (Необязательная часть, *) Изучите инструкцию в проекте и запустите web-приложение без использования docker, с помощью venv. (Mysql БД можно запустить в docker run).
4. (Необязательная часть, *) Изучите код приложения и добавьте управление названием таблицы через ENV переменную.
##    Ответ:  Ссылка на репозиторий - [Форк репозитория](https://github.com/bitsl40/shvirtd-example-python)
---

## Задача 2 (*)
Отчет сканирования [Отчет сканирования](https://github.com/bitsl40/virtd-homeworks1/blob/main/vulnerabilities.csv) 

   

## Задача 3
## Ответ
![Иллюстрация к проекту](https://github.com/bitsl40/virtd-homeworks1/blob/main/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203-3-sql.png)

## Задача 4
## Ответ
[Cсылка на fork](https://github.com/bitsl40/shvirtd-example-python)
При попытке выполнить SQL-запрос в контейнере запущенном на облачной ВМ, получаю ошибку при подключении к mysql: docker exec -ti mysql_db mysql -uroot -pYtR\qeWq4321
mysql: [Warning] Using a password on the command line interface can be insecure.
ERROR 1045 (28000): Access denied for user ‘root’@‘localhost’ (using password: YES)
При этом сервис запущен и работает.
Тоже самое на локальной машине отрабатывает без проблем. На облачной ВМ проект работает, сервисы отрабатывают, но при подключении к БД в контейнере возникает данная ошибка.
## MYSQL_ROOT_HOST="%" - в compose файле использовал
## Задача 5 (*)
1. Напишите и задеплойте на вашу облачную ВМ bash скрипт, который произведет резервное копирование БД mysql в директорию "/opt/backup" с помощью запуска в сети "backend" контейнера из образа ```schnitzler/mysqldump``` при помощи ```docker run ...``` команды. Подсказка: "документация образа."
2. Протестируйте ручной запуск
3. Настройте выполнение скрипта раз в 1 минуту через cron, crontab или systemctl timer. Придумайте способ не светить логин/пароль в git!!
4. Предоставьте скрипт, cron-task и скриншот с несколькими резервными копиями в "/opt/backup"

## Задача 6
При запуске команды dive hashicorp/terraform
Ошибка:
Image Source: docker://hashicorp/terraform
Fetching image... (this can take a while for large images)
Handler not available locally. Trying to pull 'hashicorp/terraform'...
cannot fetch image
cannot find docker client executable

## Задача 6.1
## Ответ
![Иллюстрация к проекту](https://github.com/bitsl40/virtd-homeworks1/blob/main/dockercp.png)

