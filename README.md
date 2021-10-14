# Fork Bomb

A fork bomb is a DOS (Denial of Service) attack against Linux or Unix-based system. 

A fork bomb is nothing than a bash function that get executed recursively in order to slow down or crash a system.

## Preventing Fork Bomb

You can get the current maximum process you can run in linux by typing `$ ulimit -u` or `$ ulimit -a`.

```
$ ulimit -u
63020
```

The number `63020` indicates that you can run 63020 processes. To protect your linux system from a fork bomb, you need 
to lower that number:

`$ ulimited -S -u 5000`

This command sets to `5000` the maximum number of processes you can run into your system.