```bash
pdfseparate plik.pdf plik%d.pdf
```
```bash
ls *.jpg | awk -v size=210mmx297mm '{printf "img2pdf -S %s -s %s %s -o %s.pdf\n",size,size,$1,$1}'
ls *.jpg | awk -v size=210mmx297mm '{printf "img2pdf -S %s -s %s %s -o xx%02d.pdf\n",size,size,$1,NR}'
```
```bash
pdfunite a.pdf b.pdf ab.pdf
pdfunite *.pdf @.pdf
pdfunite xx??.pdf @.pdf
```
