# Description

Function ``get_line`` use ``strlen(buf)`` to get length of buf. However, when ``buf`` starts with ``\x00``, will cause an oob read.

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

https://sourceforge.net/p/mcj/tickets/58/
