
* porównanie plików
```bash
for X in $(ls); do cmp $X /img/img13/$X; done
```

* usuniecie duplikatow
```bash
find . -type f|xargs -n 1 sha256sum |sort|awk '{if($1==p1)print "rm",$2,"#",p2;p1=$1;p2=$2}'
find . -type f|xargs -n 1 sha256sum |sort -r|awk '{if($1==p1)print "rm",$2,"#",p2;p1=$1;p2=$2}'
```

* dos2unix
```bash
find . -type f|xargs -n 1 dos2unix
```
