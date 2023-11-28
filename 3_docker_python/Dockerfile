FROM python:3.8-alpine

#COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

RUN pip install Flask

RUN pip freeze > requirements.txt

RUN pip install -r requirements.txt

COPY ./app /app

ENTRYPOINT [ "python" ]

CMD ["view.py" ]
