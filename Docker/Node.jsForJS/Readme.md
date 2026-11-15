## Node.js для JavaScript

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

> Никогда в разработке не используйте русские имена файлов и каталогов!

> Никогда в разработке не используйте пробелы и спец.символы в именах файлов и каталогов!

> Создание проекта лучше начать с "чистого листа", предварительно остановив и удалив все другие контейнеры и образы!

Запустить **Node.js REPL**
```shell
docker run -it --rm node:alpine node
```

И запустить скрипт
```shell
console.log('Hello from Docker!');
```

Для выхода из консоли
```shell
.exit
```
![1](/img/Code_JtRkYvRGTN.png)

или
```shell
docker run --rm node:alpine node -e "console.log('Hello')"
```

> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!