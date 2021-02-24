
FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E

WORKDIR /app

#Give your Repository
RUN git clone https://github.com/ahfarmer/emoji-search.git

FROM python:3

WORKDIR /app

COPY --from=repo /app/emoji-search /app 

RUN pip install flask waitress

EXPOSE 4202

CMD ["python", "./app.py"]
