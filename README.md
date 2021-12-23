# GBT
A neat repo for neat people :)

## Installing setting up virtualbox and Linux
Go here for a good tutorial on how to set up virtualbox with the latest version of Ubuntu
- https://www.wikihow.com/Install-Ubuntu-on-VirtualBox

Next, you need to install guest additions, it just helps you be able to fullscreen the virtual machine as well as helps with performace. I think this should tell you how to get it
- https://linuxize.com/post/how-to-install-virtualbox-guest-additions-in-ubuntu/

And here's some stuff to speed up the VM if it's running slow (Not sure how much it will actually help)
- http://www.rawinfopages.com/tips/2017/07/speed-up-virtualbox-in-windows/


### Alright, now you should have linux set up properly.


## Installing python and your preferred IDE
Alright so next you have to install python obviously. I have been using python 3.8 on my virtual machine, so it's probably recommended you do the same. It's okay if you're using a slightly different version of Python 3, though. Just don't use Python 3.10 as it has some issues right now
- https://www.python.org/downloads/

Then, you're going to need an IDE. I recommend PyCharm, as it is poggers. You should be able to download this by going into the app drawer (bottom left), searching "Ubuntu Software" in the search bar (should have an app store logo), launching that and searching for PyCharm. Should be a very easy download. I had some weird bugs where it looked like it wasn't downloading, but it was. Just give it some time it takes a while.

You should also go back app drawer (or whatever you call it) and find the terminal. Launch it, then right click it and select "Add to favorites". You're gonna need it 

## General Commands
Alright general commands that you'll use a lot. 

```
ls # lists files and directories

cd # change directory

cd - # go back to previous directory

mkdir dirname # creates a directory

rmdir dirname # deletes directory

rm filename # deletes a file

python3 -V # if you have python3 installed, it should return the version of python3 you have

pip # if pip is installed (which I think it should be once you have python) it will return a ton of stuff. 
This is good. This is what you'll use to install packages/modules/libraries for python
```

Alright well we should probably set up virtual environments now. You're gonna need that for python projects

You're going to want to use pip to install the virtualenv module.
```
pip install virtualenv
```
You should be able to type the command **"virtualenv"** and get a bunch of stuff returned. If not, never fear, go here for the answer (this happened to me)
- https://stackoverflow.com/questions/31133050/virtualenv-command-not-found

Now you should be able to create python virtual environments using this command.
```
virtualenv -p python3 envname
```

Here are some helpful commands for virtual environments
```
source envname/bin/activate # activates your virtual environment

deactivate # deactivates the virtual environment

pip freeze # displays all the packages installed in the environment

pip install library_name # installs a python library. If you have your virtualenv activated, it will install to that 
instead of your machine which is what we want
```

A few other things to note:
- You can tell your virtualenv is activated when you see the env name in parenthesis before your name on the command line. example below
```
trevor@trevor-VirtualBox:~/Desktop$ ls
aliases.txt  envname

trevor@trevor-VirtualBox:~/Desktop$ source envname/bin/activate
(envname) trevor@trevor-VirtualBox:~/Desktop$ pip freeze
```

When you have your virtual machine for your project activated, you should be able to run your python by typing
```
python3 project.py # runs the python project (obviously you must be in the same directory or you must add the
filepath beforehand
```

## Github commands
You should already have github installed. Type "git" in your terminal, and if it's installed it should return some stuff. If not, it should give you the command required to install it. We'll go over more github stuff later because I'm feeling lazy right now. I'll leave some commands below

```
# FYI: git commands won't work if you're not in the repository

git status # shows any changed files, which branch you are on, other stuff... Very helpful

git add file_name # adds a (changed) file to the repository

git commit -m "message" # commits all added changes to a commit

git push origin branch_name # pushes the commit to the repository
```
