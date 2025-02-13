FROM ubuntu
RUN apt-get update
RUN apt-get install -y python3 python3-pip
RUN pip install flask --break-system-packages
COPY app.py /opt/app.py
ENV FLASK_APP=/opt/app.py

ENTRYPOINT ["flask","run"]
CMD ["--host=0.0.0.0"]