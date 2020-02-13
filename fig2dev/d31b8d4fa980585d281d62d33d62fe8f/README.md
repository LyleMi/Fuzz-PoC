# Description

bound check not correct, will cause oob write in function ``read_objects`` line 459,

see asan output in ``asan.txt``.

# Step to reproduce

```
git clone https://salsa.debian.org/debian/fig2dev.git
autoreconf
./configure CFLAGS="-fsanitize=address -g"
make
./fig2dev/fig2dev -L box ./case
```

# Reference

https://sourceforge.net/p/mcj/tickets/61/
