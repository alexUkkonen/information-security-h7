## Applied Cryptography

* one way functions are functions that are easy to encrypt but "impossible" to decrypt taking many milion years with all the computing recources in the world
* trapdoor one way functions are like normal ones but there is a "secret" path that makes it easy to compute if you need to.
* Hash functions turn data (examples: image, text) in to a fixed length and potentially "scrambles" them
* One way hash functions encrypt the shortened data so that you can't decrypt it without the key
* MAC is a one way hash function with a key


## Installing and using hashcat

For this exercise i mainly followed instruictions. i will order the commands in order bellow.

```$ sudo apt-get update```


```$ sudo apt-get -y install hashid hashcat wget```


```$ mkdir hashed```


```$ cd hashed```


```$ wget https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz```


```$ tar xf rockyou.txt.tar.gz```


```$ rm rockyou.txt.tar.gz```


```$ hashid -m 6b1628b016dff46e6fa35684be6acc96```


```$ hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved```

```$ cat solved```

All of this worked well and we got the solution summer.

For the second exersice with d595b2086532422bbe654bc07ea030df i had to be creative as the text file got so long i couldn't read it anymore.

For me to be able to read it i had to install glogg

<img width="2120" height="155" alt="image" src="https://github.com/user-attachments/assets/3b8addd5-5979-448d-8c68-33924c1eba53" />

afther this you have to open the dir with cd

lastly you type ```$ glogged solved```

<img width="1884" height="241" alt="image" src="https://github.com/user-attachments/assets/025b1d81-6a25-4120-ab11-bcd37563832c" />

<img width="2068" height="1249" alt="image" src="https://github.com/user-attachments/assets/d6ef6764-7000-4b30-9686-a02f8e030b76" />

we can see the solution is "disobey"

## Sources
* https://terokarvinen.com/information-security/
* https://learning.oreilly.com/library/view/applied-cryptography-protocols/
