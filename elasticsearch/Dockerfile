# Use elastic opensource version as runtime
FROM docker.elastic.co/elasticsearch/elasticsearch:7.11.0

# Avoid error from bootstrap checks
USER root
RUN echo "discovery.type: single-node" >> /usr/share/elasticsearch/config/elasticsearch.yml
