FROM digitallyseamless/nodejs-bower-grunt:latest

EXPOSE 80

RUN mkdir /jssdk && \
    cd /jssdk    && \
    bower install qiniu

WORKDIR /jssdk/bower_components/qiniu

COPY config.js ./demo/
COPY Gruntfile.js ./

RUN make install && \
    make build

ENTRYPOINT make dev
