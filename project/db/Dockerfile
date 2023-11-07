
FROM amazonlinux:2

#初期装備をインストール
RUN yum install -y yum-utils tar wget procps epel-release

#インストール
RUN yum -y install mariadb mariadb-server

#pingコマンド使用
RUN yum install -y iputils

#port確認
EXPOSE 3306

# DB作成
RUN mkdir /var/lib/mysql/wordpress/
COPY ./wordpress /var/lib/mysql/wordpress/
RUN chown -R mysql:mysql /var/lib/mysql/wordpress

#mariadbの起動
CMD ["/usr/bin/mysqld_safe" ,"--skip-grant-tables"]

