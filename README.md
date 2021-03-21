# Dates and Time in Python
This repository explores ways of working with times and dates in Python. It explores the datetime module that comes with the standard Python library. We also look at dateparser, a third party Python package.

## Installations
You need a version of Python3.7 or above. I am currently using Python 3.9 as it is the most updated version as of mid March 2021. I had Python 3.6 installed and the .fromisoformat() method from datetime did not work. This is because I needed a later version of Python. All Python installations come with pip, a package manager, which will discussed further in this document.
On Ubuntu/Linux, to [uninstall](https://stackoverflow.com/questions/48899604/how-to-uninstall-python-in-ubuntu-completely-and-reinstalling-it) outdated versions of Python.:

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

Python on other OS's are available [here]( https://www.python.org/downloads/)

## Example Usage

Type ```python3``` and you should be taken to the Python interpreter. You can try the following out for youself to get a feel for how the different methods are used.

## Setting up your dev environment

In your terminal or command line prompt, type ```python --version``` to see that you have the appropriate version of Python is installed.
Next, wherever you store your programming documents, make a folder and go into it with the following commands: 
- `mkdir Dates`
- `cd Dates`
Then we are going to create an isolated virtual environment so that when we install third party packages, it won't take up too much space on your machine. 
To make a new virtual environment folder, simply enter ```python3 -m venv venv``` for Linux and ```python -m venv venv``` for Windows. If you enter ```ls``` or ```dir``` you should see the venv folder. Also note, if you enter ```which pip3```, it will point to the directory of the virtual environment instead of the global environment. To activate your virtual environment, enter ```source ./venv/bin/activate``` for Linux and ```venv\Scripts\activate``` for Windows. Enter ```deactive``` to exit your virtual environemnt.

Enter your virtual environment. We are going to restore requirements so that the third-party dateparser module works. Then, we are going to install dateparser with the command ```pip install -r requirements.txt```. Using this method, as oppposed to manually entering ```pip3 install [package_name]```, makes sure that the desired third-party packages, with the desired version pinning, is explicitly being used. It also makes repeatibility possible and cleanups simple.
If you enter ```pip3 list``` you will see that dateparser was installed as well as other secondary/transitive dependencies.

[image](https://user-images.githubusercontent.com/25753853/111908832-2133b700-8a31-11eb-8510-3b7d99506b48.png)

To clear up some of the space that these third party packages take up, simple run the command ```pip3 uninstall [package_name]```.





