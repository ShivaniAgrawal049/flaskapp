FROM ubuntu:18.04

RUN apt-get update -y && \
 apt-get -y install python3-dev

RUN apt-get install python3-pip -y
RUN apt-get install gunicorn3 -y

WORKDIR /app

ADD . /app

RUN pip3 install -r requirements.txt

CMD ["gunicorn3", "-b", "0.0.0.0:8000", "app:app", "--workers=5"]
