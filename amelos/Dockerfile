FROM alper/minidebjava10:v1

COPY ./amelos-jar-with-dependencies.jar /usr/src/myapp/amelos-jar-with-dependencies.jar

COPY ./langdetect-183.bin /usr/src/myapp/langdetect-183.bin

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["nice", "-n", "5", "java", "-XX:MetaspaceSize=37m", "-XX:MaxMetaspaceSize=37m", "-Xms90m", "-Xmx90m", "-XX:+UseG1GC", "-jar", "assos-jar-with-dependencies.jar", "amelos"]



