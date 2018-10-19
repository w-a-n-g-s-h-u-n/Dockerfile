FROM wangshun1024/java:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

ENV TOMCAT_MAJOR=8 \
    TOMCAT_VERSION=8.5.34 \
    CATALINA_HOME=/usr/local/tomcat \
    CATALINA_OUT=/dev/null
RUN apk add curl && \
    curl -jksSL -o /tmp/tomcat.tar.gz http://archive.apache.org/dist/tomcat/tomcat-${TOMCAT_MAJOR}/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz && \
    gunzip /tmp/tomcat.tar.gz && \
    tar -C /usr/local -xf /tmp/tomcat.tar && \
    mv /usr/local/apache-tomcat-${TOMCAT_VERSION} ${CATALINA_HOME} && \
    apk del curl && \
    rm -rf ${CATALINA_HOME}/webapps/* ${CATALINA_HOME}/bin/*.bat /tmp/* /var/cache/apk/*
ENV PATH=$CATALINA_HOME/bin:$PATH
VOLUME ["$CATALINA_HOME/logs"]
EXPOSE 8080
CMD ["catalina.sh", "run"]