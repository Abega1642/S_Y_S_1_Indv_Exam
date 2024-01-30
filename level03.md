# Level 03
---
The solution of this level 03 is still found in the directory ```/home/level```.
Now look for the directory named ```03```inside of that ```/home/level/``` directory and look what can you found in there :
```sh
yourUsername@warchll:/home/level$ ls -al
    ...
drwxrwxr-x 3 root    level03 4096 Jan 11  2023 03
    ...
yourUsername@warchll:/home/level$ cd 03/
yourUsername@warchll:/home/level/03$ ls -alR
```
Using that last command ```ls -alR``` you will see you can not find something intersing there seeing that you have no permission for some directory. But the solution of the level 02 gave us a hint. So, you have to look at the configuration hidden file named ```.bash_history``` 
```sh
yourUsername@warchll:/home/level/03$ cat .bash_history
```
Suprise, there you go !
