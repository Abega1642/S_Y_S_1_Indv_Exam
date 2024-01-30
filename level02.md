# Level 02
---
As you already now, solution can be found in ```/home/level```. So now look for the directory named ```02``` and check what's inside in integral so we won't check each directory everytime anymore :
```sh
yourUername@warchall:/home/level$ ls -al
    ...
drwxr-xr-x 5 root    level02 4096 Jan 11  2023 02
    ...
yourUsername@warchall:/home/level$ cd 02/
yourUsername@warchall:/home/level/02$ ls -alR
```

Then you will see a hidden file named ```.solution``` in a hidden directory named ```.porb``` . Read what's indide :
```sh
    ...
./.porb:
total 12
drwxr-xr-x 2 root level02 4096 Jan 11  2023 .
drwxr-xr-x 5 root level02 4096 Jan 11  2023 ..
-rw-r--r-- 1 root root      32 Jan 11  2023 .solution
    ...
yourUsername@warchall:/home/level/02$ cat .porb/.solution
```
There you go again !