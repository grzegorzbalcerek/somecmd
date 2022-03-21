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
* concat
```bash
convert img1.jpg img2.jpg -append img3.jpg
convert img1.jpg img2.jpg +append img3.jpg
```
* zdjecia rotate
```bash
ROTATE='{split($1,f,"[.]");split($3,c,"x");p=1-1.4*sin(a*3.14159/180);w=int(c[1]*p);h=int(c[2]*p);print "convert",$1,"-rotate",a,"-crop",w"x"h"+"int((c[1]-w)/2)"+"int((c[2]-h)/2),f[1]"-"a"."f[2]}'
identify 21906-kiry-133456-dsc.jpg|awk -v a=3 "$ROTATE"
```
* remove alpha channel
```bash
convert input.png -background white -alpha remove -alpha off output.png
```
* napis jako obrazek
```bash
convert -transparent white -fill black -font Arial -pointsize 20 label:zakupy@grzegorzbalcerek.org zakupy-mail.png
convert -transparent white -fill black -font Arial -pointsize 20 label:gb@grzegorzbalcerek.org gb-mail.png
```
* img split
```bash
convert -crop 50%x100% input.jpg output.jpg # output-0.jpg output-1.jpg
convert -crop 100%x50% input.jpg output.jpg
```
* img2pdf
```bash
img2pdf --pagesize A4 --output out.pdf input.jpg
img2pdf -S A4 -o out.pdf file1.jpg file2.jpg
```
