FROM python:3.7
ENV PYTHONUNBUFFERED 1
MAINTAINER michio-k

RUN mkdir /code
WORKDIR /code

ADD requirements.txt /code/
RUN pip install --no-cache-dir -r requirements.txt
ADD . /code/

# CMD ["bash","/code/startup.sh"]
# CMD ["python", "/code/connect_db.py"]
