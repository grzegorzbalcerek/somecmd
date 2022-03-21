
```bash
ARG1=$1
case $ARG1 in
    value1) echo Wartość 1;;
    value2) echo Wartość 2;;
    *) echo zla opcja; exit 1;;
esac
```
```bash
cat - > plik.txt <<EOF
$(dirname $(realpath $0))
tekst $USER $(hostname) escape: \${ZMIENNA}
# komentarz $USER
EOF
```
