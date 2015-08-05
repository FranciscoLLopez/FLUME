# FLUME
Flume sample

##Statement
The company Florists Reunidas (FR) has 50 provincial branches in Spain.
Each of these locations has a data-center that serves hundreds of
florist members. Each of florists access their systems
via a web-based application that runs on the data-center of the
headquarters. In this application every sale and every order that is performed is recorded.
This information is recorded in an application log present in each
Web servers (several per data-center, on different machines). East
log file is in the /var/log/operaciones.log route.

The log is rotated daily to a folder / var / named operations
operations- <date> .log where they are stored for analysis.

Transactions are stored in the log file in the format:
[Timestamp] [TIPO_OPERACION] [DATOS_OPERACION]

The timestamp is the epoch in universal time and there are more than twenty types
different operation. Among them are the types 'SALE' and 'ORDER'.
The data associated with a operacióno are different depending on the type of
it is concerned.

The maximum size of each of these log entries in 300 bytes. The
number of events per minute in each location is of medium 60.
All sites can be accessed by network two machines 'fr-PBX-1' and
'Fr-PBX-2' that have been installed to collect the information to a
HDFS that is only accessible from the headquarters. Ports 10000-10100
They are open for applications to use.
