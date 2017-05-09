FROM python:3
MAINTAINER Martin Peters

# create err user and set it's home as working dir
RUN mkdir -p /err/data && adduser -D -h /err err
WORKDIR /err

# define data and config.py as volumes
VOLUME /err/data /err/config.py

# install errbot
RUN pip install errbot~=5.0

# define command
USER err
CMD ['errbot']
