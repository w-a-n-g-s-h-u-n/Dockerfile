FROM wangshun1024/java:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

RUN mkdir -p /data && touch /data/app.jar
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Dsun.jnu.encoding=UTF-8 -Dfile.encoding=UTF-8 -Djava.security.egd=file:/dev/./urandom -jar /data/app.jar" ]