```bash
pdfseparate plik.pdf plik%d.pdf
```
```bash
ls *.jpg | awk -v size=210mmx297mm '{printf "img2pdf -S %s -s %s %s -o %s.pdf\n",size,size,$1,$1}'
ls *.jpg | awk -v size=210mmx297mm '{printf "img2pdf -S %s -s %s %s -o xx%02d.pdf\n",size,size,$1,NR}'
```
Połączenie plików pdf
```bash
pdfunite a.pdf b.pdf ab.pdf
pdfunite *.pdf @.pdf
pdfunite xx??.pdf @.pdf
```
Skan A4 do pdf
```bash
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 1.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 2.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 3.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 4.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 5.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 6.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 7.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 8.pdf 0.jpg; rm -f 0.jpg
(scanimage | convert - 0.jpg); img2pdf --pagesize A4 --output 9.pdf 0.jpg; rm -f 0.jpg
```
Skan A6 do pdf
```bash
(scanimage | convert - 0.jpg); img2pdf --pagesize A6 --output 1.pdf 0.jpg; rm -f 0.jpg
```
