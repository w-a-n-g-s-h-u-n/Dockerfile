FROM wangshun1024/java:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

RUN mkdir -p /data && touch /data/app.jar
ENV JAR_OPTS=" -Dsun.jnu.encoding=UTF-8 -Dfile.encoding=UTF-8 -Djava.security.egd=file:/dev/./urandom "
ENTRYPOINT [ "sh", "-c", "java $JAR_OPTS $JAVA_OPTS -jar /data/app.jar" ]