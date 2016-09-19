FROM tutum/centos:centos7
WORKDIR /opt/
RUN yum -y install go git
RUN env GOPATH=/opt/ go get github.com/xlaurent/pproxies/pproxies

ENV PORT 9527
ENV CHUNK_SIZE 5
ENV TEST_URL http://httpbin.org/ip
ENV PROXY_TIMEOUT 5
ENV TEST_TIMEOUT 5
ENV MAX_ERROR 15
ENV PROXY_NUM 5
ENV INTERVAL 5
ENV API default

CMD /opt/bin/pproxies -p $PORT -s $CHUNK_SIZE -u $TEST_URL -t $PROXY_TIMEOUT -T $TEST_TIMEOUT -e $MAX_ERROR -n $PROXY_NUM --interval $INTERVAL --api $API
