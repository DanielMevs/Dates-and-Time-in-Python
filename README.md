# Dates and Time in Python
This repository explores ways of working with times and dates in Python. It explores the datetime module that comes with the standard Python library. We also look at dateparser, a third party Python package.

## Installations
You need a version of Python3.7 or above. I had Python 3.6 installed and the .fromisoformat() method from datetime did not work. This is because I needed a later version of Python. All Python installations come with pip, a package manager, which will discussed further in this document.
On Ubuntu/Linux, to uninstall outdated versions of Python:

$ ls* https://stackoverflow.com/questions/48899604/how-to-uninstall-python-in-ubuntu-completely-and-reinstalling-it
```
 - sudo rm -rf /usr/bin/python2.x as well as python3.x
 - sudo rm -rf /usr/lib/python2.x as well as python3.x
 - sudo rm -rf /usr/local/lib/python2.x as well as python 3.x 
 ```

updating Ubuntu:
`` -sudo apt-get update``
Now download a python tgz file from https://www.python.org/downloads/ and unzip it and CD into it
```
./configure
make test
sudo make install
```
Python should be installed now. Check by running python



On other OS's: https://www.python.org/downloads/ 

