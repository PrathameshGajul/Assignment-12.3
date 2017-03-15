Q1.What is meant by FlumeNG ?
Ans:
-Flume NG is a refactoring of Flume.
-To solve certain known issues and limitations, Flume requires a refactoring of some core classes and systems. This bug is a parent issue to track the development of a "Flume NG".
-Subtasks should be added to track individual systems and components.
-The following known issues are specifically to be addressed:
1.Code complexity; Flume has evolved over the last few years and has a fair amount of extraneous code.
2.Core component lifecycle standardization and control code (e.g. anything that can be start()ed or stop()ed, sources, sinks).
3.(Static) Configuration access throughout the code base.
4.Drastic simplification of common data paths (e.g. durability as an element of the source rather than a disconnected sink).
5.Heartbeat and master rearchitecture.
6.Renaming packages to org.apache.flume.



Q2. Can Flume provides 100 % reliability to the data flow?
Ans:
-Yes, it provides end-to-end reliability of the flow.
-By default, flume uses a transactional approach in the data flow.
-Sources and sinks encapsulated in a transactional repository provides by the channels.
-These channels are responsible to paas reliably from end to end in the flow.
-So it provides 100% reliability to the data flow.



Q3.Can Flume can distributes data to multiple destinations?
Ans:
Yes,it supports multiplexing flow.
The event flows from one sources to multiple channels and multiple destinations.
It is achieved by defining a flow multiplexer.



Q4.Explain about the different channel types in Flume. And which channel type is
faster?
Ans:
The 3 different channel types available in Flume are-
-MEMORY Channel – Events are read from the source into memory and passed to the sink.
-JDBC Channel – JDBC Channel stores the events in an embedded Derby database.
-FILE Channel –File Channel writes the contents to a file on the file system after reading the event from a source. The file is deleted only  after the contents are successfully delivered to the sink.
-MEMORY Channel is the fastest channel among the three however has the risk of data loss. The channel that you choose completely depends on the nature of the big data application and the value of each event.

