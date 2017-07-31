FROM wurstmeister/storm:0.9.4
MAINTAINER Wurstmeister

RUN /bin/mkdir /usr/local/srcFolder
ADD waves-storm-0.2.0-SNAPSHOT.jar /usr/local/
ADD ../srcFolder /usr/local/srcFolder

RUN /usr/bin/config-supervisord.sh nimbus 
RUN /usr/bin/config-supervisord.sh drpc

EXPOSE 6627
EXPOSE 3772
EXPOSE 3773
ADD start-supervisor.sh /usr/bin/start-supervisor.sh

CMD /usr/bin/start-supervisor.sh
