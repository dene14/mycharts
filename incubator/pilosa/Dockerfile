FROM pilosa/pilosa:v1.1.0 as source

FROM busybox:1.29.3

LABEL maintainer "dev@pilosa.com"

COPY --from=source /pilosa /LICENSE /NOTICE /

EXPOSE 10101
VOLUME /data

ENTRYPOINT ["/pilosa"]
CMD ["server", "--data-dir", "/data", "--bind", "http://0.0.0.0:10101"]
