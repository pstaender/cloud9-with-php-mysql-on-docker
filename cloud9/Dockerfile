FROM kdelfour/cloud9-docker
# install php7 + mysql client
RUN echo 'deb http://packages.dotdeb.org jessie all' > /etc/apt/sources.list.d/dotdeb.list
RUN curl http://www.dotdeb.org/dotdeb.gpg | apt-key add -
RUN apt-get update
RUN apt-get install -y php7.0 php7.0-cli mysql-client
RUN printf "[client]\nuser=root\npassword=supersecret\nport=3306\nhost=db\n" > ~/.my.cnf
# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# cloud9 code completion: https://github.com/c9/c9.ide.language.codeintel/blob/master/README.md
ADD c9.ide.language.codeintel.sh /root/c9.ide.language.codeintel.sh
RUN chmod +x /root/c9.ide.language.codeintel.sh
RUN /root/c9.ide.language.codeintel.sh