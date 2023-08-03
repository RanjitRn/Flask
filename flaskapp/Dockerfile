RUN apt-get upgrade -y
RUN apt-get install python3-pip -y
RUN apt-get install gunicorn3 -y

COPY requirements.txt requirements.txt
COPY flaskapp /opt

RUN pip3 install -r requirements.txt

WORKDIR /opt/

EXPOSE 8000

CMD ['gunicorn3','-b','0.0.0.0:8000','app:app','--workers=5']