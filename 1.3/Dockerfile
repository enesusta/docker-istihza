FROM registry.access.redhat.com/ubi8/ubi-minimal:8.1

MAINTAINER Enes Usta <enesusta@email.com>

ARG SERVICE_NAME=defaultService
ENV SERVICE_NAME $SERVICE_NAME

WORKDIR /work/

RUN wget https://github.com/enesusta/istihza/releases/download/v1.0.3/istihza-1.0.3-linux-amd64.tar.gz
RUN tar xvfz istihza-1.0.3-linux-amd64.tar.gz
RUN rm istihza-1.0.3-linux-amd64.tar.gz
RUN chmod +x istihza-1.0.3-runner

EXPOSE 8080

USER 1001

CMD ["./istihza-1.0.3-runner", "-Dquarkus.http.host=0.0.0.0"]


