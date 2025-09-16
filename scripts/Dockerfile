FROM registry.cn-hangzhou.aliyuncs.com/huang6349/amazoncorretto:17.0.15
ADD project-gateway-*.jar /app.jar
ADD wait /wait
RUN chmod +x /wait
EXPOSE 8058
EXPOSE 8055
CMD /wait && java -Djava.security.egd=file:/dev/./urandom -Xms1024M -Xmx1024M -Xmn256m -jar /app.jar --spring.profiles.active=prod
