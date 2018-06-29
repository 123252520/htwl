FROM lwieske/java-8:jre-8u121-slim
VOLUME /tmp
ADD htwlgs-cloud-registry.jar app.jar
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENTRYPOINT ["java","-Xmx256m","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
EXPOSE 8761