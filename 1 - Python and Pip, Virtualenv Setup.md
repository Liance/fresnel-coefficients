# Session Summary

In this session we'll be setting up python, pip and making a virtual environment we can work within.

We're then going to install

## Setting up python and pip

1. Open Terminal to get access to the command line.

2. Check to see if you have some version of Python already installed.

  Type `python -V` into your command line and if it shows Python 3.X is installed, you can skip to the next section: **Installing pip**. Otherwise, just keep going with these instructions normally.

3. To install Python, copy and paste this command into your command line.

    `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

3. Then we'll install Python with the homebrew software we just installed.

  `brew install python`

  If you get permission errors, type the following in (enter each line separately and press enter).
```
sudo chown -R "$USER":admin /usr/local
sudo chown -R "$USER":admin /Library/Caches/Homebrew
```

4. Verify that Python's installed correctly.

  `python -V`

### Installing Pip

1. To install pip, we'll enter this into the command line:

  `sudo easy_install pip`

  You might get prompted to enter your password - that's fine -  `sudo` just means you want to do things as the owner of your computer, or the superuser.

### Installing Virtualenv

1. Now pip should be installed, and we can use it to install **virtualenv**, a Virtual Environment manager.

  `sudo pip install virtualenv`

### Setting up our first virtual environment

1. First we want to point our command line to where we want to install our virtual environment. Let's put it on the desktop, where it'll be easy to find. (when you get more advanced, you probably don't want to stick it on the desktop - but for now you want stuff to be transparent and easy to find)

  `cd ~/Desktop`

  `cd` here means Change Directories, and `~/Desktop` specifies that we want to change our current directory to the Desktop folder.

2. Create a new virtual environment:

  `virtualenv yourenv -p python3.6`

  `yourenv` specifies the name of the virtual environment folder. You can name it anything you want, but calling it `yourenv` is fine for now.

3. Activate virtualenv - this tells the command line we want to step into the virtual environment. You can only do this when your command line is in your virtual environment folder.

  `source bin/activate`

If you've done this correctly, your command line prompt (the little prompt that always shows up in the terminal) should look like this:

`(yourenv) Airbuds-iMac:~ airbud$`

Great! You're now set up and working within a virtual environment.

If you want to leave it and go back to your system environment, you can try `deactivate` or `source deactivate`, or simply close your current command line session and open a new Terminal, and you'll be back in your base system environment again.

4. Let's practice re-entering the virtual environment. Close the Terminal window, and open a new one. Notice how your prompt has changed so you're no longer in the virtual environment.

5. We need to point our command line to the virtual environment folder before we activate it.

  Move to your desktop.

  `cd ~/Desktop`

  And from there, we can perform `ls` to see what folders are on the desktop. Our virtual environment folder should be among the folders and files lsited.

  Enter by typing:

  `cd yourenv`

  or whatever you called it earlier.

6. Activate the virtual environment.

  `source bin/activate`

  And your prompt should now show that your virtual environment is active.


## Conclusion

We've installed Python, and we've set up pip so we can install Python packages. We now also know how to set up virtual environments and activate them, and we've used the command line to do all of this.

Now we're ready to install the packages we'll need.
