# flume-ftp-source
------------------

This forked version of ftp-flume.source is linked against flume-1.5.0.

### Notes:

ftp-source relies on local serialization to keep track of processed files, this means that ftp-source cannot be operated in several agents in parallel with the same ftp source.

## Configuration

It take the following config properties:

| Property            | Default   | Description                                                         |
| --------------------|-----------|---------------------------------------------------------------------|
| name.server         |    -      | the name of your server                                             |
| user                |    -      | user name                                                           |
| password            |    -      | the password                                                        |    
| run.discover.delay  |    -      | polling delay for new files                                         |
| port                |    21     | the port of the ftp server                                          |
| flushLines          |    true   | will flush individual lines instead of the entire file in 1k chunks |


## Version history
------------------

0.0.2       introduced line oriented event flushing



## TO DOs:
------------------

- introduce exclusion patterns for files
