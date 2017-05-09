FROM python:3-alpine
MAINTAINER Martin Peters

# create err user
RUN mkdir -p /err/data && adduser --home /err err
WORKDIR /err

VOLUME /err/data /err/config.py

RUN pip install errbot~=5

USER err
CMD ['errbot']
