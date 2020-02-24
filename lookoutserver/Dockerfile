FROM java:8

VOLUME /tmp

ADD lookout-all-1.6.0.snapshot.jar app.jar

RUN bash -c 'touch /app.jar'

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-Dcom.alipay.sofa.ark.master.biz=lookoutall","-jar","/app.jar"]