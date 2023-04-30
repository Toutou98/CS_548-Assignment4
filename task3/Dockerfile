FROM python:slim-buster

RUN apt-get update && \
    apt-get upgrade -y

COPY requirements.txt controller.py /app/

WORKDIR /app

RUN pip install -r requirements.txt

CMD python3 controller.py