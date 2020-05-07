FROM logstash:5.5-alpine

ENV PLUGIN_BIN "/usr/share/logstash/bin/logstash-plugin"
ENV ES_JAVA_OPTS "-Xms128m -Xmx128m"
RUN "$PLUGIN_BIN" install logstash-input-syslog
RUN "$PLUGIN_BIN" install logstash-filter-date
RUN "$PLUGIN_BIN" install logstash-filter-grok
RUN "$PLUGIN_BIN" install logstash-filter-useragent
RUN "$PLUGIN_BIN" install logstash-output-elasticsearch

COPY ./conf /etc/logstash

CMD ["-f", "/etc/logstash/logstash.conf"]
