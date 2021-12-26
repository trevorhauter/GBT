# GBT
A neat repo for neat people :) (Gianni Bryan Trevor)

Below is a bunch of instructions on everything you need for python development on Ubuntu using virtual box. I'm going to lay out the steps and helpful information, and I'll probably put a bunch of links for trouble shooting at the bottom, so if you have trouble on any of the steps look down there.

# Installing and setting up virtualbox with Ubuntu (Linux)
1. Go [here](https://www.wikihow.com/Install-Ubuntu-on-VirtualBox) for a good tutorial on how to set up virtualbox with the latest version of Ubuntu, our preferred flavor of linux

2. Now you need to [install guest additions](https://linuxize.com/post/how-to-install-virtualbox-guest-additions-in-ubuntu/), it just helps you be able to fullscreen the virtual machine as well as helps with performace. If that isn't helpful, go [here](https://www.nakivo.com/blog/make-virtualbox-full-screen/) (be sure to go to the linux section) and let me know so I can switch these links around. (Note: the sudo user in linux is just like an admin)

3. (optional) If you want to try speeding up your VM, take a look at [this](http://www.rawinfopages.com/tips/2017/07/speed-up-virtualbox-in-windows/)


Alright, now you should have linux set up properly. You should be able to run the virtual machine full screen at proper resolution and play around with linux!


# Installing python and your preferred IDE
Next you have to install [python](https://www.python.org/downloads/). I have been using python 3.8 on my virtual machine, so it's probably recommended you do the same. It's okay if you're using a slightly different version of Python 3, though. Just don't use Python 3.10 as it has some issues right now. If you have trouble with the python.org link, try this [one](https://docs.python-guide.org/starting/install3/linux/).

You're also going to need an IDE. I recommend PyCharm, as it is poggers. You should be able to download this by going into the app drawer (bottom left), searching "Ubuntu Software" in the search bar (should have an app store logo), launching that and searching for PyCharm. Should be a very easy download. I had some weird bugs where it looked like it wasn't downloading, but it was. Just give it some time it takes a while.

You should also go back app drawer (or whatever you call it) and find the terminal. Launch it, then right click it and select "Add to favorites". Basically just adding it to your taskbar. You'll need it a lot 

# General Linux Commands to use in the Terminal
Here are some general commands that you'll use a lot. It's important to note that a lot of these commands (like cd for example) can be used with more parameters and can do more than I'm listing here, I'm just showing the basics

## Linux Commands

```
ls # lists files and directories

ls -a # lists all the files and directories (including hidden). Helpful for finding .gitignore


    To navigate into the root directory, use "cd /"
    To navigate to your home directory, use "cd" or "cd ~"
    To navigate up one directory level, use "cd .."
    To navigate to the previous directory (or back), use "cd -"

cd / # navigate to the root directory

cd or cd ~ # navigate to your home directory

cd .. # navigate up one directory level, use

cd - # navigate to the previous directory (or back)

mkdir dirname # creates a directory

rmdir dirname # deletes directory

rm filename # deletes a file

cat filename # prints the context of a file

touch filename # creates an empty file

nano filename # nano is a text editor that can be used in the terminal

ctrl + c # interupts whatever is running in the terminal (like python code)

ctrl + d # closes terminal window
```
[Here](https://linuxize.com/post/how-to-use-nano-text-editor/) is a link where you can learn a little bit about nano. You'll mostly just be using it to add/edit text, and saving and exiting out. It's relatively intuitive. Use nano instead of vim or other text editors unless you're a genius

# Python, virtual environments and github
Commands and information on setting up and using python with virtual environments and github. 
A brief overview:
- virtualenv is a tool used to create isolated Python environments. It creates a folder which contains all the necessary executables to use the packages that a Python project would need (i.e. libraries)
- github is what we are on now. It contains the project and allows us to all colaborate on something. Very poggers.

## Python and pip commands
```
python3 -V # shows the version of python3 you are using

pip -V # shows the version of pip you are using

pip install libraryname # install a library

pip freeze > requirements.txt # creates a text file that contains all the libraries required for your project

pip install -r /path/to/requirements.txt # installs all requirements noted in the text file
```

## Virtual Environments

First, use pip to install the virtualenv library by running this command.
```
pip install virtualenv
```
Now, you should be able to type the command **"virtualenv"** and get a bunch of stuff returned. If not, never fear, go [here](https://stackoverflow.com/questions/31133050/virtualenv-command-not-found) for the answer (this happened to me)

Now you should be able to create python virtual environments using this command.
```
virtualenv -p python3 envname
```

Here are some helpful commands for virtual environments
```
source envname/bin/activate # activates your virtual environment

deactivate # deactivates the virtual environment

pip freeze # displays all the packages installed in the environment

pip install libraryname # installs a python library. NOTE: If you have your virtualenv activated, it will 
install to that instead of your machine which is what we want
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
python3 project.py # runs a py file
```

### Github commands
You should already have github installed. Type "git" in your terminal, and if it's installed it should return some stuff. If not, it should give you the command required to install it. We'll go over more github stuff later because I'm feeling lazy right now. I'll leave some commands below

```
# Note: git commands won't work if you're not in the repository

git status # shows any changed files, which branch you are on, other stuff... Very helpful

git branch # shows available branches

git checkout branch_name # checks out a branch

git checkout -b branch_name # creates a branch with the given name

git add file_name # adds a (changed) file to the repository

git commit -m "message" # commits all added changes to a commit

git push origin branch_name # pushes the commit to the repository

git pull # pulls in changes that have been pushed to github
```

# Random help links
- [Python style guide (pep 8)](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds)
- [Using geckodriver with linux](https://askubuntu.com/questions/870530/how-to-install-geckodriver-in-ubuntu)
- [Setting up a vritual environment](https://stackoverflow.com/questions/22288569/how-do-i-activate-a-virtualenv-inside-pycharms-terminal)
- [More in depth info abot virtual environments in python](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/)
- [Aliases in linux/ubuntu](https://unix.stackexchange.com/questions/215948/how-to-make-an-alias-permanent) (Note: we use bash)
