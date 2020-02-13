# Description

Function ``read_textobject`` use ``strlen(s)`` to get length of ``s`` in line 1355. However, when ``s`` starts with ``\x00``, will cause an oob read.

see asan output in ``asan.txt``.

# Step to reproduce

```
git clone https://salsa.debian.org/debian/fig2dev.git
autoreconf
./configure CFLAGS="-fsanitize=address -g"
make
./fig2dev/fig2dev -L box ./case
```
    
