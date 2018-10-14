## Bandit Level 0
* ssh

```
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
=> bandit0@bandit.labs.overthewire.org's password:
bandit0
```

## Bandit Level 1
* dashed filename

```
$ ssh bandit10@bandit.labs.overthewire.org -p 2220
=> bandit1@bandit.labs.overthewire.org's password:
boJ9jbbUNNfktd78OOpsqOltutMc3MY1

$ cat ./-
```

Bandit Level 2
* spaces in filename
```
$ ssh bandit20@bandit.labs.overthewire.org -p 2220
=> bandit2@bandit.labs.overthewire.org's password:
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

$ vim "./spaces in this filename"
```

Bandit Level 3
* hidden file
```
$ ssh bandit30@bandit.labs.overthewire.org -p 2220
=> bandit3@bandit.labs.overthewire.org's password:
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

$ bandit3@bandit:~$ ls
$ cd inhere/
$ ls -al
$ cat .hidden
```

Bandit Level 4
* identify file types
```
$ ssh bandit40@bandit.labs.overthewire.org -p 2220
=> bandit4@bandit.labs.overthewire.org's password:
$ pIwrPrtPN36QITSp3EQaw936yaFoFgAB

$ file inhere/*
$ cd inhere
$ cat ./-file07
```

Bandit Level 5
* search for files that matched the exact size
* 1033 byte
* find

```
$ find ./inhere -size 1033c
$ cat ./inhere/maybehere07/.file2
```

* [find 指令介紹](http://man.linuxde.net/find)
* -size 大小單位
  * b —— 512 bytes
  * c —— byte
  * w —— 2 bytes
  * k —— kilo
  * M —— mega
  * G —— giga