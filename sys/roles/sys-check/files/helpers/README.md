
Get first level shared libs, procedure should be recurce
most times 2 levels enought

```
ldd ncrack.x86_64 | awk '{print $3}' | grep '/' | xargs -IX -n 1 cp X ./
ldd ncrack.x86_64 | awk '{print $3}' | grep '/' | xargs -n 1 ldd |  awk '{print $3}' | grep '/' | sort -u | xargs -n 1 -IX cp X ./
```
