
* zdjecia w index.html
```bash
ls *.JPG *.jpg | awk '
BEGIN { print "<html><body>"}
{ print "<p><img src="$1"><br/>"$1"</p>"}
END { print "</body><html>" }' > index.html
```

* zmniejsz pliki i zapisz w podkatalogu
```bash
export ARG1=20
test -n "$ARG1" || {echo "Give percentage as argument";exit 1;}
mkdir -p $ARG1
ls *.jpg | awk '{print "convert",$1,"-resize","'$ARG1'%","x/"$1}'
```
