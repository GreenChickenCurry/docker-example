# Примеры Docker Контейнеров

## О Практике

Для трёх различных веб-приложений были написаны три докер контейнера:


* 1_docker_spring,
* 2_docker_dotnet,
* 3_docker_python.


Первый, второй и третий контейнеры содержат соответственно spring boot(java), dotnet(C#) и flask(python) веб-приложения.

Каждый Dockerfile написан соблюдая Best Practicies. 
Некоторые контейнеры написаны с использованием многоступенчатой сборки(multi-stage builds)
для оптимизации, лёгкости чтения и поддержки.

Для запуска соответствующего контейнера заходим в соответствующую директорию и прописываем в терминал:

* Для 1_docker_spring:
```sh
  docker build -t test1:latest .
```
```sh
  docker run -d -p 8080:8080 test1:latest
```

* Для 2_docker_dotnet:
```sh
  docker build -t test2:latest .
```
```sh
  docker run -d -p 5000:5000 test2:latest
```

* Для 3_docker_python:
```sh
  docker build -t test3:latest .
```
```sh
  docker run -d -p 5001:5001 test3:latest
```

Далее переходим в браузере на

```sh
  http://localhost:[port]
```
