# pyOSClogger
A simple Python OSC logger.

pyOSClogger would save all OSC messages received on the designated OSC port to a tab-separated text file .
Only two messages are not logged as they are used to control the logger:

- /start <filename> would start logging OSC messages to a file called <filename>_<timestamp>.txt
  <timestamp> format is yyyy-mm-dd_hh-mm-ss
- /stop would cease logging and save the file.

Every message is timestamped with the current time, with microseconds resolution.

Sample output file contents:

```
30-07-16 00-25-34.826176	/acc	0.34	0.17	0.4
30-07-16 00-25-35.325870	/acc	0.1	0.32	0.91
30-07-16 00-25-35.826011	/acc	1	0.2	10
30-07-16 00-25-35.826966	/word	somestring
30-07-16 00-25-36.326174	/acc	0.28	0.5	0.22
30-07-16 00-25-36.326541	/word	anotherstring
30-07-16 00-25-36.825849	/acc	0.55	0.09	0.0
30-07-16 00-25-36.826683	/word	yetanotherstring
```