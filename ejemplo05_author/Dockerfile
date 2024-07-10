#GENERAR LA IMAGEN
# docker build -t ejemplo05_author .
# docker tag app-authors just5ebas/ejemplo05_author --> en caso no se quiera generar la imagen desde 0
# docker build -t just5ebas/ejemplo05_author .

# docker login
#docker push just5ebas/ejemplo05_author

FROM eclipse-temurin:17.0.11_9-jre-jammy

RUN mkdir /app
WORKDIR /app

COPY build/quarkus-app/app ./app
COPY build/quarkus-app/lib/ ./lib
COPY build/quarkus-app/quarkus/ ./quarkus
COPY build/quarkus-app/quarkus-run.jar app.jar

CMD ["java","-jar","app.jar"]