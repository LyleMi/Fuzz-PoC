# heap buffer overflow on getlong

## Step to reproduce

```bash
export CFLAGS="-g -fsanitize=address"
./configure
make
./src/xls2csv ./case
```

## reference

https://www.wagner.pp.ru/~vitus/software/catdoc/
source http://ftp.wagner.pp.ru/pub/catdoc/catdoc-0.95.tar.gz
