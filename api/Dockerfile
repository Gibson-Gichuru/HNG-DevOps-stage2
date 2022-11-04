FROM python:3.8-buster

RUN groupadd -r HNG && useradd -r -g HNG HNG

RUN chsh -s /usr/sbin/nologin root

WORKDIR /home/api

COPY requirements.txt requirements.txt

RUN pip install --upgrade pip && pip install -r requirements.txt

COPY . .
