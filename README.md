# flume-agent-fq
  flume agent which allows perform fuzzy query on incoming data.

### Author: ET, ASz, MU

# Getting started
  At first download flume binaries from:
  http://flume.apache.org/download.html
  Solution has been tested on version 1.9.

### Configuration:
  This conf files put into /conf directory of bin version of flume. Logger can be set in log4j.properites
  I recommend use:
 * *flume.root.logger=INFO,console* because output of sink is displayed in console.
 * *flume.root.logger=DEBUG,console* in case of any probles use: 

### Additional libraries:
  Additional libraries put into /lib directory with .jar extension.
  List of additional lib: 

### Run flume:
  Run command in main catalog.
  **for Windows:**
  * bin/flume-ng agent -n agent -c conf -f conf/flume.properites
  
  Command should create the agent composed of source, channel and sink.
  * source.type = http -> recive http requests
  * channel.type = memory -> channel created in memory, it doesn't save results
  * sink.type = logger -> displays results in console.

requests: POST with JSON in body:
[{
  "headers" : {
             },
  "body" : "random_body"
  },
  {
  "headers" : {
             },
  "body" : "really_random_body"
  }]
  
