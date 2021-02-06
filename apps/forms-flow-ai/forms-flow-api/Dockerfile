FROM python:3.8

ADD . /forms-flow-api/app
WORKDIR /forms-flow-api/app

RUN pip install --upgrade pip
RUN pip install psycopg2

RUN pip install .

RUN mkdir /nltk_data && chmod 777 /nltk_data

EXPOSE 5000
RUN chmod u+x ./entrypoint
ENTRYPOINT ["/bin/sh", "entrypoint"]
