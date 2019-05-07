### Linux常用命令备忘

* ##### 目录下文件按大小排序

```
ls -lrt | sort -n -r -k5

Note: -r为逆序，-k5表示为按第五行的数据排序

  -g, --general-numeric-sort  compare according to general numerical value
  -i, --ignore-nonprinting    consider only printable characters
  -M, --month-sort            compare (unknown) < 'JAN' < ... < 'DEC'
  -h, --human-numeric-sort    compare human readable numbers (e.g., 2K 1G)
  -n, --numeric-sort          compare according to string numerical value
  -R, --random-sort           sort by random hash of keys
      --random-source=FILE    get random bytes from FILE
  -r, --reverse               reverse the result of comparisons
      --sort=WORD             sort according to WORD:
                                general-numeric -g, human-numeric -h, month -M,
                                numeric -n, random -R, version -V
```

* ##### 目录下文件按大小排序\(包括文件夹\)

```
du -s * | sort -n -k1

du -sh * | sort -h -r
```

* bash通配符使用

```
hogan@hogan:~/Downloads$ du -sh * | grep [0-9]G
3.9G    rom
14G    Tools
```

* ##### 执行前一条命令并替换部分参数

```
hogan@hogan:~/Documents$ ls -lrth *.py
ls: cannot access *.py: No such file or directory
hogan@hogan:~/Documents$ ^py^txt
ls -lrth *.txt
-rw-rw-r-- 1 hogan hogan 1.5K Dec 6 2017 tc_cp_cmd.txt
```

* ##### 快速查看ASCII码

```
man ascii
```

* ##### SimpleHttpServer

https://docs.python.org/2/library/simplehttpserver.html

https://docs.python.org/3/library/http.server.html

```
* Python2
python -m SimpleHTTPServer 8000

* Python3
python3 -m http.server 8000
```



