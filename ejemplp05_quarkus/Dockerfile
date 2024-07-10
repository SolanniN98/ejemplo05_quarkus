#GENERAR LA IMAGEN
# docker build -t ejemplp05_quarkus .
# docker tag app-authors just5ebas/ejemplp05_quarkus --> en caso no se quiera generar la imagen desde 0
# docker build -t just5ebas/ejemplp05_quarkus .

# docker login
#docker push just5ebas/ejemplp05_quarkus

FROM eclipse-temurin:17.0.11_9-jre-jammy
#FROM bellsoft/liberica-runtime-container:jdk-17-glibc

RUN mkdir /app
WORKDIR /app

COPY build/quarkus-app/app ./app
COPY build/quarkus-app/lib/ ./lib
COPY build/quarkus-app/quarkus/ ./quarkus
COPY build/quarkus-app/quarkus-run.jar app.jar

CMD ["java","-jar","app.jar"]