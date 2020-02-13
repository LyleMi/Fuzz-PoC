# Description

this input will construct a error format ``F_spline``, will free error memory.

see asan output in ``asan.txt``.

# Step to reproduce

```
git clone https://salsa.debian.org/debian/fig2dev.git
autoreconf
./configure CFLAGS="-fsanitize=address -g"
make
./fig2dev/fig2dev -L box ./case
```
    
