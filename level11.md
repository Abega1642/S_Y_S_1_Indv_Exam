# Level 11 :
---
# _Choose your Path II_
---
---
As written in the subject of this challenge, the answer will be found in ```/home/level/11_choose_your_path_2```. In this level 11, we are given an C prgramme named ```charp2.c``` which can be executed through ```charp2```as we can see in this directory mentionned above :
```sh
yourUsername@warchall:/home/level/11_choose_your_path2$ ls -al
    ... 
-rwxr-sr-x  1 level11 level11 16440 Jan  4  2023 charp2
-rw-r--r--  1 root    level11  1987 Jan  4  2023 charp2.c
-rwxr-xr-x  1 root    level11    86 Jan  4  2023 compile2.sh
-rw-r-----  1 root    level11   297 Jan  4  2023 solution.txt
    ...
```
After reading the the ```charp2.c```and try to use ```./charp2``` we can understand that this program count the number of character by line of each file that is put in argument of ```./charp2```. When we read carefully the ```charp2.c```code we can see that the code uses a function `escape_single_quotes` to escape single quotes in the filename. This function replaces each occurrence of the character `'` with `'\''`. So, we should find a way to exploit that . But The source code ensures secure handling of file names by escaping single quotes. This is particularly important when using system commands, especially with options such as `--files0-from=`, which process file names separated by null characters.

In fact, the `--files0-from=` option employs null-terminated strings as separators in a file containing a list of paths. This approach enhances the robustness and reliability of handling filenames with spaces or special characters

So, the best way is to try to execute the program `./charp2` using the instruction `--files0-from=`

Now, type the command  :
```sh
yourUsername@warchall:/home/level/11_choose_your_path2$ ./charp2 "--files0-from=solution.txt"
```
There you go and got it !