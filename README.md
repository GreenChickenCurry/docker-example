# docker-example

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
