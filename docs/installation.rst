=======================
nvPY installation guide
=======================

There are many (mostly very easy) ways to install nvPY. This document summarises a number of them.

Windows step-by-step for beginners
==================================

Following this recipe, you'll first install Python for win32 (this also works on Windows 64!), then Python setuptools and pip, and then nvpy itself.

1. Download and install (by double-clicking) the Python 2.7.3 Windows Installer: http://python.org/ftp/python/2.7.3/python-2.7.3.msi
2. Download and install (by double-clicking) Python setuptools: http://pypi.python.org/packages/2.7/s/setuptools/setuptools-0.6c11.win32-py2.7.exe
3. Start a command shell by pressing Windows-R and typing "cmd" followed by enter into the input box that appears.
4. At the command shell prompt, type the following::

    \Python27\Scripts\easy_install pip
    \Python27\Scripts\pip install nvpy

5. In c:\\users\\yourlogin\\ create a file called nvpy.cfg, using your favourite text editor, with the lines::

    [nvpy]
    sn_username = your_simplenote_email
    sn_password = your_simplenote_password

6. From now on, start nvpy by double-clicking on "nvpy.exe" in c:\\Python27\\Scripts\\ -- consider creating a shortcut to this on your desktop or in your start menu.

For curious users: The magic invocation in step 4 automatically downloads and installs both pip and nvpy. We could have skipped the pip installation, installing nvpy directly with easy_install, but having pip around is useful in the future.

Ubuntu / Mint / Debian step-by-step #1
======================================

On Debian-flavoured systems with apt, this generally works::

    sudo apt-get install python python-tk python-pip
    sudo pip install nvpy

Create a file in your home directory called .nvpy.cfg with just the following contents::

    [nvpy]
    sn_username = your_simplenote_email
    sn_password = your_simplenote_password

To start nvpy, just do::

    nvpy

Advanced users
==============

You can obviously run nvpy directly from a git repo. Start with::

    git clone git://github.com/cpbotha/nvpy.git
    cd nvpy
    python nvpy
    
Don't forget to create .nvpy.cfg in your home directory before you start nvpy.

