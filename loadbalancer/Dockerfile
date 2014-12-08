FROM dockerfile/haproxy

# Install serf
WORKDIR /usr/src/app
RUN apt-get update -q
RUN apt-get install -qy build-essential git supervisor unzip
ADD https://dl.bintray.com/mitchellh/serf/0.6.3_linux_amd64.zip /usr/src/app/serf.zip
RUN unzip serf.zip
RUN mv serf /usr/bin/serf
RUN rm serf.zip

# Run haproxy
CMD ["bash", "/haproxy-start"]
