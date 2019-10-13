FROM maven:3.6.2-jdk-12

ENV PROJECT_DIR=/app

COPY ./ $PROJECT_DIR

WORKDIR $PROJECT_DIR/backend
RUN mvn dependency:go-offline

WORKDIR $PROJECT_DIR/config-server
RUN mvn dependency:go-offline

WORKDIR $PROJECT_DIR/eureka
RUN mvn dependency:go-offline

WORKDIR $PROJECT_DIR/util
RUN mvn dependency:go-offline

WORKDIR $PROJECT_DIR/zuul-service-gateway
RUN mvn dependency:go-offline

RUN rm -Rf /app
