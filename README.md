# binlogEventStats

A fake slave that generates stats over the binary log streaming.

## Requirements

All you need is:

```
pip install mysql-replication
```

## Want to help?

Read the [docs](https://python-mysql-replication.readthedocs.org/en/latest/).


## Limitations

Use `binlog_format = row`, otherwise it will explode in your face.


## Have fun!

```
sysbench --test=oltp --mysql-port=22695 --mysql-host=127.0.0.1 \
  --mysql-user=msandbox --mysql-password=msandbox --mysql-db=test prepare

sysbench --test=oltp --mysql-port=22695 --mysql-host=127.0.0.1 \
    --mysql-user=msandbox --mysql-password=msandbox --mysql-db=test run
```


## Future applications

The idea is to trace all the events and debug events in the binary logs:
https://www.percona.com/blog/2016/06/03/binary-logs-make-mysql-5-7-slower-than-5-6/
