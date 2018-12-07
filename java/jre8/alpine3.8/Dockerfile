FROM frolvlad/alpine-oraclejre8
MAINTAINER wangshun <wangshun@wangshun.org>

ENV LANG=zh_CN.UTF-8 \
    JAVA_HOME=$JAVA_HOME/jre
RUN echo "http://mirrors.aliyun.com/alpine/v3.8/main" > /etc/apk/repositories \
    && echo "http://mirrors.aliyun.com/alpine/v3.8/community" >> /etc/apk/repositories \
    && apk update upgrade \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo "Asia/Shanghai" > /etc/timezone