FROM Ubuntu:latest

RUN apt-get update
RUN apt-get install python

RUN pip insatll flask
RUN pip install flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run

# docker build Dockerfile -t mycustom-app