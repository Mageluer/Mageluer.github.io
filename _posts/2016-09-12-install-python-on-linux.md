---
layout: post
title: Install python on Linux
nav: true
categories: computer
tags: Python
---

## Check the version
Python runs on many operating systems such as MS-Windows, Mac OS, Mac OS X, Linux, FreeBSD, OpenBSD, Solaris, AIX, and many varieties of free UNIX like systems. The latest version of CentOS, Fedora, RHEL and Ubuntu come with **Python 2.7** out of the box. 

![](https://cdn.fedoramagazine.org/wp-content/uploads/2015/11/Python_logo.png)

To see which version of Python you have install, open a command terminal and run:

{% highlight bash %}
$ python --version
{% endhighlight %}

Sample outputs:

{% highlight bash %}
Python 2.7.11
{% endhighlight %}

Or type:

{% highlight bash %}
$ python
{% endhighlight %}

Sample outputs:

{% highlight bash %}
Python 2.7.11 (default, Aug  9 2016, 15:45:42) 
[GCC 5.3.1 20160406 (Red Hat 5.3.1-6)] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> 
{% endhighlight %}

That is the version of python you have got and you can start building Python applications .

## Use package manager
The easiest way to install the Python is to use package manger such as apt-get, yum, and so on.

### Debian / Ubuntu Linux user
Use the following command to search for available versions of Python2.x under Debian and Ubuntu Linux:

{% highlight bash %}
$ apt-cache search python | egrep "^python2.[0-9] " --color
{% endhighlight %}

Type the following command to install python version 2.x:

{% highlight bash %}
$ sudo apt-get install python2.6
{% endhighlight %}

Type the following command to install python version 3.x:

{% highlight bash %}
$ sudo apt-get install python3.1
{% endhighlight %}

Sample outputs:

{% highlight bash %}
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  python3.1-minimal
Suggested packages:
  python3.1-doc python3.1-profiler
The following NEW packages will be installed:
  python3.1 python3.1-minimal
0 upgraded, 2 newly installed, 0 to remove and 13 not upgraded.
Need to get 5,444 kB of archives.
After this operation, 19.9 MB of additional disk space will be used.
Do you want to continue [Y/n]? y
Get:1 http://debian.osuosl.org/debian/ squeeze/main python3.1-minimal amd64 3.1.3-1 [1,669 kB]
Get:2 http://debian.osuosl.org/debian/ squeeze/main python3.1 amd64 3.1.3-1 [3,775 kB]
Fetched 5,444 kB in 27s (201 kB/s)
Selecting previously deselected package python3.1-minimal.
(Reading database ... 280220 files and directories currently installed.)
Unpacking python3.1-minimal (from .../python3.1-minimal_3.1.3-1_amd64.deb) ...
Selecting previously deselected package python3.1.
Unpacking python3.1 (from .../python3.1_3.1.3-1_amd64.deb) ...
Processing triggers for man-db ...
Processing triggers for menu ...
Processing triggers for desktop-file-utils ...
Processing triggers for gnome-menus ...
Setting up python3.1-minimal (3.1.3-1) ...
Setting up python3.1 (3.1.3-1) ...
Processing triggers for menu ...
{% endhighlight %}

### Red Hat/ RHEL / CentOS Linux user
Type the following command:

{% highlight bash %}
$ sudo dnf install python
{% endhighlight %}

OR

{% highlight bash %}
# dnf install python
{% endhighlight %}

## From the Internet
Your can also download the version you want from the Internet.

Type the following command to download it:

{% highlight bash %}
$ wget --no-check-certificate https://www.python.org/ftp/python/2.7.11/Python-2.7.11.tgz
{% endhighlight %}

Type the folowing command to extract the file and go into the directory:

{% highlight bash %}
$ tar -xzf Python-2.7.11.tgz  
$ cd Python-2.7.11
{% endhighlight %}

Read the README file to figure out how to install, or do the following with no guarantees:

{% highlight bash %}
$ ./configure  
$ make  
$ sudo make install  
{% endhighlight %}

For Python 3.5 use the following download address:  <http://www.python.org/ftp/python/3.5.1/Python-3.5.1.tgz>

For other versions and the most up to date download links:  <http://www.python.org/getit/>

## Others

### Setuptools & Pip
The two most crucial third-party Python packages are [setuptools](https://pypi.python.org/pypi/setuptools) and [pip](https://pip.pypa.io/en/stable/).

Python 2.7.9 and later (on the python2 series), and Python 3.4 and later include pip by default.

To see if pip is installed, open a command prompt and run:

{% highlight bash %}
$ command -v pip
{% endhighlight %}

To install pip, follow [the official pip installation guide](https://pip.pypa.io/en/latest/installing/) - this will automatically install the latest version of setuptools.

### Environment variable
Also add the path of new python in 'PATH' environment variable. 

Type the following command if new python is in `/root/python-2.7.4`:

{% highlight bash %}
$ export PATH = "$PATH":/root/python-2.7.4
{% endhighlight %}
