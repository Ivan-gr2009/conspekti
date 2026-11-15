## Metasploitable2 docker

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

> Никогда в разработке не используйте русские имена файлов и каталогов!

> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

> Создание проекта лучше начать с "чистого листа", предварительно остановив и удалив все другие контейнеры и образы!

```
Metasploitable2 — специально уязвимая виртуальная машина Linux, созданная проектом Metasploit. Предназначена для использования в качестве среды обучения и тестирования для специалистов и энтузиастов в области безопасности, чтобы практиковать навыки взлома и пентеста.
```

Установить докер-образ

```shell
docker pull tleemcjr/metasploitable2
```
![1](/img/Code_VxGzmwTy9F.png)

Загрузить образ, создать и запустить контейнер, войти в него (для Windows)
```shell
docker run --name metasploitable2 -it tleemcjr/metasploitable2
```
![2](/img/explorer_G4aHrlcodS.png)

Загрузить образ, создать и запустить контейнер, войти в него (для Linux)
```shell
docker run --name metasploitable2 -it tleemcjr/metasploitable2:latest sh -c "/bin/services.sh && bash"
```

Остановить контейнер и выйти из него
```shell
exit
```

Удалить контейнер
```shell
docker rm metasploitable2
```

Удалить образ
```shell
docker rmi tleemcjr/metasploitable2
```
![3](/img/Code_vxRcOGUYy7.png)

[Metasploitable2 на Docker hub](https://hub.docker.com/r/tleemcjr/metasploitable2#!)

> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору! 