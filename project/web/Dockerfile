
#AmazonLinux2の環境を使用
FROM amazonlinux:2

#初期装備をインストール
RUN yum -y install yum-utils tar wget procps epel-release
RUN yum clean all

#Apacheインストール
RUN yum -y install httpd

#PHPのインストール
RUN amazon-linux-extras enable php7.3
RUN yum install -y php php-gd php-mysqlnd php-xmlrpc

#wordpressインストール
#ENV wpdl https://wordpress.org/latest-ja.tar.gz

# wp download
#RUN cd /var/www/html && wget -O - $wpdl | tar xzfv -
#RUN mv /var/www/html/wordpress/* /var/www/html
RUN wget https://wordpress.org/latest.tar.gz
RUN tar -xzvf latest.tar.gz
RUN mv /wordpress/* /var/www/html
RUN chown -R apache:apache /var/www/html
RUN chmod 2775 /var/www/html

CMD [ "/usr/sbin/httpd", "-D", "FOREGROUND" ]
