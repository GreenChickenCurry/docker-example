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

Заходим в директорию \textup{Dockerdir}, далее, в папку \textup{1\_docker\_spring}.
	Теперь запускаем следующие команды:
	\begin{verbatim}
		docker build -t test1:latest .
		docker run -d -p 8080:8080 test1:latest
	\end{verbatim}
	После этого заходим в браузер и заходим на:
	\begin{verbatim}
		http://localhost:8080
	\end{verbatim}
