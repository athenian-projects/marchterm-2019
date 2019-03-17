# Unix commands

* How are these different?

```bash
$ date | wc -l
$ date | wc -w
$ date | wc -c
$ date | wc -lwc
$ date | wc
```

```bash
$ date | sleep 1 | wc 
$ sleep 1 | date | wc 
```

```bash
$ date > now.txt
$ wc -l now.txt
$ cat now.txt | wc -l
```

* Create a file named `test.txt`:
```bash
$ cat > test.txt
a
b
c
a
b
c
Ctrl-D

$ ls test.txt
test.txt

$ ls -l test.txt
-rw-r--r--  1 pambrose  staff  12 May 24 16:25 test.txt

$ cat test.txt
a
b
c
a
b
c
```

* How do these command sequences differ?

```bash
$ cat test.txt | wc -l
$ cat test.txt | uniq | wc -l
$ cat test.txt | sort | wc -l
$ cat test.txt | uniq | sort | wc -l
$ cat test.txt | sort | uniq | wc -l
$ cat test.txt test.txt test.txt | sort | wc -l
$ cat test.txt test.txt test.txt | sort | uniq | wc -l
```
