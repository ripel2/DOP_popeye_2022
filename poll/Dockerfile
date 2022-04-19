FROM python:3.9-buster
LABEL author="Lucas Hauszler"

RUN mkdir -p /app

COPY . /app/
WORKDIR /app
COPY app.py .

RUN pip3 install -r requirements.txt

EXPOSE 80

CMD [ "flask", "run", "--host=0.0.0.0", "--port=80" ]
