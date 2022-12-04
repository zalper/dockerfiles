FROM alper/minidebjava10:v1

COPY ./ReplazFat-jar-with-dependencies.jar /usr/src/myapp/ReplazFat-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["nice", "-n", "5", "java", "-XX:MetaspaceSize=20m", "-XX:MaxMetaspaceSize=20m", "-Xms11m", "-Xmx11m", "-XX:+UseG1GC", "-jar", "ReplazFat-jar-with-dependencies.jar", "APP_TYPE__ServiceMonitor", "cunda"]



