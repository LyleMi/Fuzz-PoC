# Description

see asan output in ``asan.txt``.

# Step to reproduce

```
git clone https://git.code.sf.net/p/mcj/fig2dev
git checkout 639c36010a12
autoreconf
./configure CFLAGS="-fsanitize=address -g"
make
 ./fig2dev -L pictex ./poc
```

# reference

https://sourceforge.net/p/mcj/tickets/83/
