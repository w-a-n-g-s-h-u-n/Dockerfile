FROM wangshun1024/jar:jre8
MAINTAINER wangshun <wangshun@wangshun.org>

COPY agent /opt/skywalking/agent/
ENV JAR_OPTS="$JAR_OPTS -javaagent:/opt/skywalking/agent/skywalking-agent.jar"