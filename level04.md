# Level 04
---
As we know solution may be found in ```/home/level```. Now, if we read the list of all directory in that directory, we can see a directory named ```04_kwisatz```. So, first read what is inside.
```sh
yourUsername@warchall:/home/level$ ls -al
    ...
drwxr-xr-x  2 root    root    4096 Feb 11  2023 04_kwisatz
    ...
yourUsername@warchall:/home/level$ cd 04_kwisatz/
yourUsername@warchall:/home/level/04_kwisatz$ ls -al
```
You will find there a file named ```README.nfo``` that tells us to look in our ```~```. In fact, in our ```~```, there is a directory named ```level```. So, check what can you find there :
```sh
yourUsername@warchall:~$ ls -l
    ...
drwxr-xr-x 3 yourUsername yourUsername 4096 Jan 10 15:22 level
    ...
yourUsername@warhchall:~$ cd level/
```
Suprise there is a same directory in there named ```04_kwisatz```. Check what's inside that directory. Read the file named ```README.txt```. That file tells you that there is something in ```README.md```.But there is a problem. You can't read it immediatly. But, by chance, you own that file so you can change the permission but make sure you are the only one who can see it.
```sh
yourUsername@warhcall:~/level/04_kwisatz$ chmod 700 README.md
yourUsername@warchall:~/level/04_kwisatz$ cat README.md
```
There you go again !