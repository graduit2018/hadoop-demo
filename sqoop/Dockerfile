FROM bde2020/hadoop-base

ENV SQOOP_HOME /usr/local/sqoop

RUN curl -Lo /tmp/sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz https://archive.apache.org/dist/sqoop/1.4.7/sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz && \
    mkdir -p /tmp/sqoop && \
    tar -xvf /tmp/sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz -C /tmp/sqoop && \
    rm /tmp/sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz && \
    mv /tmp/sqoop/sqoop-1.4.7.bin__hadoop-2.6.0 $SQOOP_HOME

RUN curl -Lo /tmp/mysql-connector-java-5.1.46.tar.gz https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.46.tar.gz && \
    mkdir -p /tmp/jdbc && \
    tar -xvf /tmp/mysql-connector-java-5.1.46.tar.gz -C /tmp/jdbc && \
    rm /tmp/mysql-connector-java-5.1.46.tar.gz && \
    mv /tmp/jdbc/mysql-connector-java-5.1.46/mysql-connector-java-5.1.46-bin.jar $SQOOP_HOME/lib/

ENV PATH $PATH:$SQOOP_HOME/bin
