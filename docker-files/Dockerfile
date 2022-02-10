FROM python:3.8-alpine3.14

RUN apk update && apk upgrade && \
    apk --no-cache --progress add mariadb-dev \
    mariadb-client \
    gcc \
    libc-dev \
    jpeg-dev \
    zlib-dev 

COPY requirements.txt ./

RUN pip3 install --no-cache --upgrade pip
#RUN pip3 install -U setuptools
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

WORKDIR /app
