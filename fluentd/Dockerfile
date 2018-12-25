FROM fluent/fluentd:v1.3.0-debian

#RUN apt-get update;apt-get install -y ruby-full

RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-rdoc", "--no-ri", "--version", "2.0.0"]

EXPOSE 24224
