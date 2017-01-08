##Anayse Web logs
Tells the most popular web file using the web access logs of the user.It uses Cloudera's opensourse Hadoop system(CDH) for storing and processing of the file.

###Usage
* Unzip `data/access_log` and place in same directory with same name.
* Add data/access_log to HDFS by `hadoop fs -put data/access_log`.Move it to `myinput` directory by `hadoop fs -mkdir myinput` then `hadoop fs -mv access_log myinput`
* Start processing using mapper and reducer by first go to `code` directory then `hs mapper.py reducer.py myinput myoutput` 
* For viewing results: `hadoop fs -cat myoutput/part-00000 | less` , the last line shows the most popular web file and total GET requests it recieved.
