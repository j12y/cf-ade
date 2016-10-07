FROM j12y/cf-ade
MAINTAINER Jayson DeLancey <jayson.delancey@ge.com>

# Install some Ubuntu dependencies
RUN apt-get update && apt-get install -y \
    python-pip \
    python-dev \
    libpq-dev

# Install Python requirements
COPY requirements.txt /tmp
RUN pip install --upgrade pip
RUN pip install --requirement /tmp/requirements.txt

