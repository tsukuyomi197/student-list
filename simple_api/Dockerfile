FROM python:3.8-buster
MAINTAINER bao (nguyenbaotrung920@yahoo.com)
COPY ./student_age.py /
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
COPY ./requirements.txt /
RUN pip3 install -r /requirements.txt
RUN mkdir -p /data && rm -rf /data/*
COPY ./student_age.json /data
EXPOSE 5000
ENTRYPOINT [ "python3", "./student_age.py"]