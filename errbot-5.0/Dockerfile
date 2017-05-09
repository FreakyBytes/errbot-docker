FROM python:3
MAINTAINER Martin Peters

# create err user and set it's home as working dir
RUN useradd --home-dir /err err
RUN mkdir -p /err/data
WORKDIR /err

# add config.py
ADD config.py /err/config.py

# define data as volume
VOLUME /err/data

# install errbot
RUN pip install errbot~=5.0

# define command
USER err
CMD ['errbot']
