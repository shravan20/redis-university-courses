Strings are the most basic kind of Redis value. Redis Strings are binary safe, this means that a Redis string can contain any kind of data, for instance a JPEG image or a serialized Ruby object.

A String value can be at max 512 Megabytes in length.

You can do a number of interesting things using strings in Redis, for instance you can:

- Use Strings as atomic counters using commands in the INCR family: INCR, DECR, INCRBY.
- Append to strings with the APPEND command.
- Use Strings as a random access vectors with GETRANGE and SETRANGE.
- Encode a lot of data in little space, or create a Redis backed Bloom Filter using GETBIT and SETBIT.

Redis strings commands are used for managing string values in Redis. Following is the syntax for using Redis string commands.

Syntax

```js
redis 127.0.0.1:6379> COMMAND KEY_NAME 
```

Example
```js
redis 127.0.0.1:6379> SET user:101:time-zone UTC-8 EX 7200 //Expiry Time 7.2k secs
OK 
redis 127.0.0.1:6379> GET user:101:time-zone 
"UTC-8"
redis 127.0.0.1:6379> INCR user:101:visit-counts 
1 
redis 127.0.0.1:6379> INCRBY user:101:visit-counts 40 
41 
```