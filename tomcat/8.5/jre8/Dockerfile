FROM wangshun1024/java:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

ENV TOMCAT_MAJOR=8 \
    TOMCAT_VERSION=8.5.34 \
    TOMCAT_NAME=apache-tomcat \
    CATALINA_HOME=/usr/local/$TOMCAT_NAME \
    CATALINA_OUT=/dev/null \
    PATH=$CATALINA_HOME/bin:$PATH

RUN apk add curl && \
    curl -jksSL -o /tmp/${TOMCAT_NAME}.tar.gz http://archive.apache.org/dist/tomcat/tomcat-${TOMCAT_MAJOR}/v${TOMCAT_VERSION}/bin/${TOMCAT_NAME}-${TOMCAT_VERSION}.tar.gz && \
    gunzip /tmp/${TOMCAT_NAME}.tar.gz && \
    tar -C /usr/local -xf /tmp/${TOMCAT_NAME}.tar && \
    ln -s ${CATALINA_HOME}-${TOMCAT_VERSION} ${CATALINA_HOME} && \
    rm -rf ${CATALINA_HOME}/webapps/* && \
    apk del curl && \
    rm -rf /tmp/* /var/cache/apk/*

VOLUME ["$CATALINA_HOME/logs"]
EXPOSE 8080
CMD ["catalina.sh", "run"]