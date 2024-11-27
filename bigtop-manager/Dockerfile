FROM rockylinux:8

RUN yum -y install sudo wget openssh-clients openssh-server vim net-tools chrony krb5-server krb5-libs krb5-workstation python3 procps-ng
RUN wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz -O /tmp/jdk.tar.gz --no-check-certificate \
  && mkdir -p /usr/local/java && tar -xzf /tmp/jdk.tar.gz -C /usr/local/java --strip-components=1 \
  && rm -f /tmp/jdk.tar.gz \
  && ln -s /usr/local/java/bin/java /usr/bin/java

ENV JAVA_HOME="/usr/local/java"

COPY bigtop-manager-server /opt/bigtop-manager
