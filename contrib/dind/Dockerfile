FROM docker:24.0.5-dind-alpine3.18
WORKDIR /root/
RUN apk --no-cache add git && \
  git clone https://github.com/openfaas/faas
WORKDIR /root/faas/


EXPOSE 8080
EXPOSE 9090

COPY entry.sh .
RUN chmod +x ./entry.sh

CMD ["./entry.sh"]
