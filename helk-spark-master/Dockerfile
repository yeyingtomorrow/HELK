# HELK script: HELK Spark Master Dockerfile
# HELK build version: 0.9 (Alpha)
# Author: Roberto Rodriguez (@Cyb3rWard0g)
# License: BSD 3-Clause

FROM cyb3rward0g/helk-spark-base:2.3.0
LABEL maintainer="Roberto Rodriguez @Cyb3rWard0g"
LABEL description="Dockerfile base for HELK Spark Master."

ENV DEBIAN_FRONTEND noninteractive

ADD scripts/spark-master-entrypoint.sh ${SPARK_HOME}/

ENV SPARK_MASTER_HOST helk-spark-master
ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG $SPARK_HOME/logs

RUN mkdir -p $SPARK_MASTER_LOG

EXPOSE 8080 7077
WORKDIR $SPARK_HOME
ENTRYPOINT ["./spark-master-entrypoint.sh"]