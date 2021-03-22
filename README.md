# Dates and Time in Python

Dealing with time as a programmer can be tricky, especially if you take into account leap seconds, time-zone inconsistencies, culture influences, and more. This repository explores Python's great built-in modules such as time for time-related functions where dates are not needed. It also has a datetime module that supplies classes for manipulating dates and times. Calendar is another module that outputs calendars and provides functions using an idealized Gregorian calendar. We also look at dateparser, a third party Python package that packs a punch in terms of processing natural language. 

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

The following shows the time module. Time in the time module is a datetime object. It has a method named time that returns the number of seconds since the UNIX epoch. As this file is being editted, that number is approximately 1616431766.3649557. This instant occured on Janruary 1st, 1970 and is what almost all computers count time from. 

![image](https://user-images.githubusercontent.com/25753853/112026271-67aa1400-8b0c-11eb-90ac-4aa815f15578.png)

The datetime module is designed to make it less complicated to access attributes of the object related to dates, times, and timezones. These objects include __datetime.date__ which stores the *year*, *month*, and *day* atrributes. __datetime.time__ stores *hour*, *minute*, *second*, *microsecond*, and *tzinfo* (time zone information). __datetime.datetime__ is a combination of date and time. The following shows how to create datetime instances:

![image](https://user-images.githubusercontent.com/25753853/112034278-acd24400-8b14-11eb-81cb-cbe5b80bcff9.png)

Other methods that datetime provides are __datetime.today()__ that creates a datetime instance with the current local date. __datetime.now()__ creates a datetime.datime instance with the current local date and time. __datetime.combine()__ combines instances of datetime.date and datetime.time into a single datetime.datetime instance. The following snippet shows an example.

![image](https://user-images.githubusercontent.com/25753853/112041669-0b032500-8b1d-11eb-9a35-336ca0ea98ed.png)

Python also allows you to you create datetime instances from a string in ISO 8601 format using the .fromisoformat() method.

![image](https://user-images.githubusercontent.com/25753853/112038496-4b60a400-8b19-11eb-9605-a3cd31842c4b.png)

If your string is not in ISO-8401 format, you can always use the .strptime() method. This method uses a special mini-language to tell Python which parts of the string are associated with the *datetime* attributes. The following is an example:

![image](https://user-images.githubusercontent.com/25753853/112043146-bcef2100-8b1e-11eb-8b55-675e41d2fb8e.png)

Other ways of creating datetime instances involve third party packages like dateparser (see *Development Setup* for more details). Dateparser is a library which allows you to provide natural language inputs. The follwoing is an example.

![image](https://user-images.githubusercontent.com/25753853/112047833-23c30900-8b24-11eb-9f5f-81b836d25cbb.png)

## Setting up your dev environment

In your terminal or command line prompt, type ```python --version``` to see that you have the appropriate version of Python is installed.
Next, wherever you store your programming documents, make a folder and go into it with the following commands: 
- `mkdir Dates`
- `cd Dates`

Then we are going to create an isolated virtual environment so that when we install third party packages, it won't take up too much space on your machine. 
To make a new virtual environment folder, simply enter ```python3 -m venv venv``` for Linux and ```python -m venv venv``` for Windows. If you enter ```ls``` or ```dir``` you should see the venv folder. Also note, if you enter ```which pip3```, it will point to the directory of the virtual environment instead of the global environment. To activate your virtual environment, enter:
 ```source ./venv/bin/activate``` for Linux  ```venv\Scripts\activate``` for Windows. Enter ```deactive``` to exit your virtual environemnt.

Enter your virtual environment. We are going to restore requirements so that the third-party dateparser module works. Then, we are going to install dateparser with the command - ```pip install -r requirements.txt```. 

Using this method, as oppposed to manually entering ```pip3 install [package_name]```, makes sure that the desired third-party packages, with the desired version pinning, is explicitly being used. It also makes repeatibility possible and cleanups simple.
If you enter ```pip3 list``` you will see that dateparser was installed as well as other secondary/transitive dependencies.

[image](https://user-images.githubusercontent.com/25753853/111908832-2133b700-8a31-11eb-8510-3b7d99506b48.png)

To clear up some of the space that these third party packages take up, simple run the command ```pip3 uninstall [package_name]```.





