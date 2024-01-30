# Level 00 :
---
After a succesfull log in via ssh on warchall.net, first thing to do is to check around using this command below :
```sh
yourUsername@warchall:~$ ls -al
```
You will see a file named "WELCOME.md". Read it to see instructions through this command :
```sh
yourUsername@warchall:~$ cat WELCOME.md
    ...
    ...
You will find the solution to each level in
/home/level
or
/home/user/yournick/level
    ...
    ...
```
As you can see, solutions will be found on "/home/level". So you need to check that directory using this command below :
```sh
yourUsername@warchall:~$ cd /home/level/
```
Then use this command to see what's in there :
```sh
yourUsername@warhchall:~$ ls -al
```
You will see a directory named "00_welcome" :
```sh
drwxr-xr-x  2 root    root    4096 Dec 30  2022 00_welcome
```
Then look what's inside and read the file named "README.md" :
```sh
yourUsername@warchall:~$ ls -al
...
-rw-r--r--  1 root root  522 Dec 30  2022 README.md
yourUsername@warchall:~$ cat README.md
```
There you go.





