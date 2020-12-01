FROM mysql:5.7
# add a database
ENV MYSQL_DATABASE test
ENV MYSQL_ROOT_HOST %
ENV MYSQL_ROOT_PASSWORD root
EXPOSE 3306
COPY ./init_script.sql /docker-entrypoint-initdb.d/