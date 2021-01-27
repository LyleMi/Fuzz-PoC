# Description

Triggered when `bbdNumBlocks` is set to a large value

## Step to reproduce

```bash
git clone http://www.wagner.pp.ru/git/oss/catdoc.git
export CFLAGS="-fsanitize=address -g"
./configure --prefix=`pwd`/build
mkdir build
make && make install
./build/bin/catppt ./case
```
