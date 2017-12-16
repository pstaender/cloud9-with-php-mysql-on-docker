FROM kdelfour/cloud9-docker
RUN echo 'deb http://packages.dotdeb.org jessie all' > /etc/apt/sources.list.d/dotdeb.list
RUN curl http://www.dotdeb.org/dotdeb.gpg | apt-key add -
RUN apt-get update
RUN apt-get install -y php7.0 php7.0-cli