
```bash
emacs -batch wiersze.txt -eval "(sort-lines nil (point-min) (point-max))" -f save-buffer
emacs -batch input.html -eval "(set-buffer-file-coding-system 'utf-8)" -f save-buffer
```
