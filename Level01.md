# Level 01 :
---
As you have seen in the last level (level 00), you can find solution in ```/home/level``` . So enter in that directory and look for a directory named ```01_choice_tree```.
```sh
yourUsername@warchall:~$ cd /home/level
yourUsername@warchall:/home/level$ ls -al
    ...
drwxr-xr-x  5 root    root    4096 Feb  1  2023 01_choice_tree
    ...
```
Check what's inside  that directory. There are lots of directory and file there. So you should check all of them in the same time using a unique command.
```sh
yourUsername@warchall:/home/level$ cd 01_choice_tree
yourUsername@warchall:/home/level$ ls -alR
    ...
./blue/hats/grey/solution/patience:
total 12
drwxr-xr-x 2 root root 4096 Feb 11  2023 .
drwxr-xr-x 3 root root 4096 Feb  1  2023 ..
-rw-r--r-- 1 root root   89 Feb 11  2023 SOLUTION.txt
    ...
```
Now look what's inside that file ```SOLUTION.txt``` :
```sh
yourUsername@warchall:/home/level$ cat blue/hats/grey/solution/patience/SOLUTION.txt
```
There you go !
