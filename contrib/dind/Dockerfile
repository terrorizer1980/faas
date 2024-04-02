FROM docker:26.0.0-dind-alpine3.19
WORKDIR /root/
RUN apk --no-cache add git && \
  git clone https://github.com/openfaas/faas
WORKDIR /root/faas/


EXPOSE 8080
EXPOSE 9090

COPY entry.sh .
RUN chmod +x ./entry.sh

CMD ["./entry.sh"]
