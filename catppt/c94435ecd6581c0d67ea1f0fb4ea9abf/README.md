# Description

Triggered when `msat_size` is set to a large value

## Step to reproduce

```bash
git clone http://www.wagner.pp.ru/git/oss/catdoc.git
export CFLAGS="-fsanitize=address -g"
export LDFLAGS="-g -fsanitize=address"
./configure --prefix=`pwd`/build
mkdir build
make && make install
./build/bin/catppt ./case
```
