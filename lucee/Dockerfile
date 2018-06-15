FROM lucee/lucee5:5.0.1.85

LABEL author="Quinncuatro@gmail.com"

# Documentation on Lucee Dockerfile's is here:
#   https://github.com/lucee/lucee-dockerfiles

# TOMCAT CONFIGS --> OPTIONAL to implement if you need custom Tomcat config.
COPY config/lucee/setenv.sh /usr/local/tomcat/bin/

# Lucee server configs --> OPTIONAL
COPY config/lucee/lucee-web.xml.cfm /opt/lucee/web/

# COPY IN a prepared Lucee server XML file --> OPTIONAL
COPY config/lucee/lucee-server.xml /opt/lucee/server/lucee-server/context/

# Default connection to a local MySql database.
# Use these environment variables to set up a datasource in lucee-server.xml
# -- {env:projectName_DSN_Driver}
ENV projectName_DSN_DRIVER=MySQL \
projectName_DSN_CLASS=org.gjt.mm.mysql.Driver \
projectName_DSN_CONNECTIONSTRING=jdbc:mysql://projectName-db:3306/projectName?useUnicode=true&characterEncoding=UTF-8&useLegacyDatetimeCode=true \
projectName_DSN_DATABASENAME=projectName \ 
projectName_DSN_USERNAME=root \
projectName_DSN_PASSWORD=default \
LUCEE_TIMEZONE=America/New_York

# copy code folder to /var/www
COPY code/ /var/www/