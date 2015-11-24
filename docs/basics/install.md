



## INSTALL WINDOWS 7/8 (CYGWIN ONLY)

Fully working instructions to install all dependencies on windows (using cygwin)

Before installing, please make sure you have a compiler installed.
It is needed for "pycrypto" module.
Here is a list of cygwin packages you may install to get a working compiler:

```
- libgcc
- gcc-core
- gcc-g++
- colorgcc
```

install python 2.7

install other dependencies:

```
easy_install --upgrade pip
pip install fabric
pip install ecdsa
pip install pycrypto
pip install configparser
```

After that you will need to add a $CMDCENTER_DATAHOME env var

Then append _bin path to $PATH



## INSTALL MACOSX

Fully working instructions to install all dependencies on macosx

```
python --version && sudo easy_install --upgrade pip && sudo -H pip install fabric && sudo -H pip install ecdsa && sudo -H pip install pycrypto && sudo -H pip install configparser
```

After that you will need to add a $CMDCENTER_DATAHOME env var

Then append _bin path to $PATH




## INSTALL UBUNTU 14.04 LTS


Run this in your terminal to install dependencies

```
python --version && sudo apt-get -y install python-pip && sudo -H pip install fabric && sudo -H pip install ecdsa && sudo -H pip install pycrypto && sudo -H pip install configparser
```


After that you will need to add a $CMDCENTER_DATAHOME env var:

```
export CMDCENTER_DATAHOME="$HOME/.cmdcenter/data"
```

Then append _bin path to $PATH

```
export PATH="$HOME/.cmdcenter/src/scripts/_bin:$PATH"
```


