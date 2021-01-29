Redis keys commands are used for managing keys in Redis. Following is the syntax for using redis keys commands.

Redis keys commands are used for managing keys in Redis. Following is the syntax for using redis keys commands.

Syntax
```js
redis 127.0.0.1:6379> COMMAND KEY_NAME
```

Example
```js
redis 127.0.0.1:6379> SET keyName keyValue 
OK 
redis 127.0.0.1:6379> GET keyName 
keyValue
redis 127.0.0.1:6379> EXISTS keyName 
1
redis 127.0.0.1:6379> DEL keyName 
(integer) 1
redis 127.0.0.1:6379> UNLINK keyName
(integer) 1
```

In the above example, DEL se the command, while tutorialspoint is the key. If the key is deleted, then the output of the command will be (integer) 1, otherwise it will be (integer) 0.

