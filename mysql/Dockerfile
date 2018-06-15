FROM mysql:5.7.18

LABEL author="Quinncuatro@gmail.com"

# Default MySQL Settings
ENV MYSQL_ROOT_PASSWORD=default \
MYSQL_USER=dev \
MYSQL_PASSWORD=default \
MYSQL_DATABASE=projectName 

COPY database_sample_data.sql /docker-entrypoint-initdb.d/database_sample_data.sql