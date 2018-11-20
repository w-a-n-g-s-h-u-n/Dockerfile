FROM wangshun1024/java:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

RUN mkdir -p /data && touch /data/app.jar
CMD ["/data/app.jar"]
ENTRYPOINT [ "sh", "-c", "java", "-jar", $JAVA_OPTS, "-Djava.security.egd=file:/dev/./urandom" ]