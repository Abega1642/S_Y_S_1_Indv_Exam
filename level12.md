# Level 12 
---
# _Py-tong_
---
---


The subject of this chapiter Py-tong level 12 of this warchall is based on analyzing a python code in the file named ```pytong.py```which can be executed with the file ```pytong``` in the directory ```/home/level```under the directory ```12_pytong```.
```sh
yourUsername@warchall:/home/level$ ls -al
    ...
drwxr-xr-x  2 level12 level12 4096 Feb 20  2023 12_pytong
    ...
yourUsername@warchall:/home/level$ cd 12_pytong/
yourUsername@warchall:/home/level/12_pytong$ ls -al
    ...
-rwxr-sr-x  1 level12 level12 16184 Feb 20  2023 pytong
-rwxr-xr-x  1 level12 level12  1542 Jan  8  2023 pytong.py
-rw-r-----  1 level12 level12    40 Jan  8  2023 pytong_solution.php
    ...
 ```
 When we analyse the python code in ```pytong.py``` we can summarize this following statement : >>   This program takes in argument a file; then analyse the content of that file and save that content in ```jjk```then close the file and re-open it and read the content of the file again and save the content in ```kwisatz```. Then the program check wether the content of ```jjk```and ```kwisatz```are same or not. If yes, the program will close and that's it. But if the content of ```jjk```is different of ```kwisatz```content then we got the solution of this level 12.
 
 
 So, after documentation on php code, I got an idea.
 
 The purpose is to create a file in which its content changes everytime we open it. So, consits at creating a file which contains different thing inside between two time  _t_ and _t+dt_, where _dt_ is the time _t_ differential.

So, here is the steps : 
-   write a php code (or in other language but in my case I used php because the serveur has php module) that write a string like "_test-_"in a file for example named```level12_solution.txt``` in a miillion times so as every time we open the file it contains different things
-   execute that code in background so as we can open the file with ```./pytong```.

For my case I used this php code :
```sh
<?php
$fh = fopen("/home/user/abega/level12_solution.txt", "a");
for ($i = 0; $i < 1000000; $i++) {
        fwrite($fh, "test-");
}
fclose($fh);
?>
```
But instead of ```/home/user/abega/level12_solution.txt```you do ```/home/user/yourUsername/level12_solution.txt```
Then execute the php code and lunch ```./pytong```with ```level12_solution.txt```as its argument.

But you need to execute the python program just seconds after executing the php code in background using```&```. So after creating that php code in a file named ```test.php```for example go to the ```/home/level/12_pytong```to execute it so as you don't miss it.

```sh
yourUsername@warchall:/home/level/12_pyton$ php ~/test.php &
yourUserrname@warchall:/home/level/12_pytong$ ./pytong ~/level12_solution.txt
```

There you go! Did it! A very long process but did it!