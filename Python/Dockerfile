
FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E

WORKDIR /app

#Give your Repository
RUN git clone https://github.com/render-examples/flask-hello-world.git

FROM python:3

WORKDIR /app

COPY --from=repo /app/flask-hello-world /app 

RUN pip install flask flask_cors waitress

EXPOSE 4202

CMD ["python", "./app.py"]
