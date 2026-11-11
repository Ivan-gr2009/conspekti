## Apache

> Никогда в разработке не используйте русские имена файлов и каталогов!

> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

> Создание проекта лучше начать с "чистого листа", предварительно остановив и удалив все другие контейнеры и образы!

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

Получить образ, создать и запустить контейнер:
```shell
docker run -d --name my-apache -p 8081:80 httpd
```
![1](/img/Code_G8keehgSYQ.png)

[Откройте адрес http://localhost:8081 в браузере](http://localhost:8081)

### Редактирование веб-страницы

Зайти в контейнер
```shell
docker exec -it my-apache bash
```

Установить текстовый редактор командной строки Micro:
```shell
apt update && apt install -y micro
```
![3](/img/Code_oYtnzSt2vn.png)
![4](/img/Code_tdBcjBKyvZ.png)

Открыть файл `index.html` для редактирования содержимого
```shell
micro /usr/local/apache2/htdocs/index.html
```
![5](/img/Code_gtsArK0AFw.png)

> Чтобы в веб-странице поддерживался русский язык, вставьте тэг `<meta charset="UTF-8">`
![6](/img/Code_TUEdlPtara.png)

отредайтируйте и сохраните по `Ctrl+S` и выйти из режима редактирования по `Ctrl+Q` или `F10`

[Проверьте результат по адрес http://localhost:8081](http://localhost:8081)
![7](/img/chrome_FHQrWE6oKC.png)

Выйти из контейнера:
```shell
exit
```
![8](/img/Code_DkuQckFCAm.png)