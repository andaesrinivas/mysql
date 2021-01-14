FROM ubuntu:20.04
RUN apt-get update
#FROM mysql/mysql-server:5.7
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
COPY my.cnf /etc/mysql/my.cnf

ENV MYSQL_ROOT_PASSWORD 123

# Add a database to mysql - blogs database should be crated when the container $
ENV MYSQL_DATABASE blogs


ENV MYSQL_USER srini
ENV MYSQL_PASSWORD srinivas



# Add a database to mysql - blogs database should be crated when the container created.
ENV MYSQL_DATABASE blogs

# Copy the SQL scripts into docker-entrypoint-initdb.d/ which will execute automatically during container start up
# COPY ./script.sql/ /docker-entrypoint-initdb.d/

#ADD script.sql /docker-entrypoint-initdb.d/
#COPY ./script.sql/ /docker-entrypoint-initdb.d/script.sql/ 
VOLUME /script.sql
EXPOSE 3306 
CMD ["mysqld", "start"]
