# syntax=docker/dockerfile:1

FROM python:3.7-alpine

WORKDIR /FlightDeals

RUN apk add --no-cache git gcc musl-dev linux-headers libpq-dev
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

ENV AWS_DEFAULT_REGION=us-east-1
ENV AWS_ACCESS_KEY_ID=insert-credentials-aws
ENV AWS_SECRET_ACCESS_KEY=insert-credentials-aws
ENV AWS_SESSION_TOKEN=insert-credentials-aws

EXPOSE 5000

CMD ["flask", "run"]
