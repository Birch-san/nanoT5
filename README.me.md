# Setup

## Create virtual environment

### [Option 1]: virtualenv

```bash
python3.11 -m venv venv
source ./venv/bin/activate
pip install wheel
pip install --upgrade pip
```

### [Option 2]: conda

```bash
conda create -n nanot5 python=3.11
conda activate nanot5
```

## Install dependencies

```bash
pip install -r requirements.txt
```

You may need to copy lzma2 runtime lib into your python shared objects directory?

```bash
# https://stackoverflow.com/a/72828943/5257399
sudo apt-get install lzma
sudo apt-get install liblzma-dev
sudo apt-get install libbz2-dev
# sigh
sudo cp /usr/lib/python3.11/lib-dynload/_bz2.cpython-311-x86_64-linux-gnu.so /usr/local/lib/python3.11/
sudo cp /usr/lib/python3.11/lib-dynload/_lzma.cpython-311-x86_64-linux-gnu.so /usr/local/lib/python3.11/
```