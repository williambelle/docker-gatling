FROM ubuntu:22.04

ARG gatling=3.8.3

RUN \
  apt update && \
  apt install -yqq --no-install-recommends \
    openjdk-17-jre unzip wget && \
  rm -rf /var/lib/apt/lists/*

RUN useradd --create-home --shell /bin/bash --uid 1000 gatling
USER gatling

ENV GATLING_VERSION $gatling
ENV GATLING_HOME /home/gatling/gatling

RUN \
  mkdir -p "$GATLING_HOME" && \
  wget -q -O /tmp/gatling-$GATLING_VERSION.zip \
  https://repo1.maven.org/maven2/io/gatling/highcharts/gatling-charts-highcharts-bundle/$GATLING_VERSION/gatling-charts-highcharts-bundle-$GATLING_VERSION-bundle.zip && \
  unzip /tmp/gatling-$GATLING_VERSION.zip -d /tmp && \
  mv /tmp/gatling-charts-highcharts-bundle-$GATLING_VERSION/* $GATLING_HOME/ && \
  rm -rf /tmp/gatling*

VOLUME ["$GATLING_HOME/conf", "$GATLING_HOME/results", "$GATLING_HOME/user-files"]

ENV PATH $GATLING_HOME/bin:$PATH

WORKDIR $GATLING_HOME

ENTRYPOINT ["gatling.sh"]
