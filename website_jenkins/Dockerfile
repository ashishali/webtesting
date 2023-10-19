FROM python:3

ENV DockerHOME=/home/app/webapp

RUN mkdir -p $DockerHOME

WORKDIR $DockerHOME

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
RUN pip install django

COPY . $DockerHOME

EXPOSE 8000

CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]