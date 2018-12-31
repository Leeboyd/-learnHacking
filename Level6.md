## Bandit Level 6 -> 7

* advanced `find`
* find 目錄 -user 使用者 -group 群組 -size 大小單位 -type 類型
* [shell程序中 2> /dev/null 代表什么意思？](https://www.zhihu.com/question/53295083)

```
// owned by user bandit7
// owned by group bandit6
// 33 bytes in size

$ find / -user bandit7 -group bandit6 -size 33c -type f

// 但出現很多錯誤
// adding `2>/dev/null` to the end of our search
// tell system to output the STDERR to /dev/null
// 詳請請看上方文章

$ find / -user bandit7 -group bandit6 -size 33c -type f 2>/dev/null

$ cat /var/lib/dpkg/info/bandit7.password
```
