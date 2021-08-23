# How install Python 3.8 on Ubuntu?

![](https://arquivo.devmedia.com.br/marketing/img/guia-python-37024.png)

> When I try to install Python 3.8 terminal says it done but when i run python --version it say Python 3.7?
(base) user@admin:~$ sudo apt-get install python3.8
Reading package lists... Done
Building

As per the instructions on [How to Install Python 3.8 on Ubuntu, Debian and LinuxMint – TecAdmin](https://tecadmin.net/install-python-3-8-ubuntu/), try the following:

### Prerequisites:

Install \[and or update\] the following packages; build-essential, checkinstall, libreadline-gplv2-dev, libncursesw5-dev, libssl-dev, libsqlite3-dev, tk-dev, libgdbm-dev, libc6-dev, libbz2-dev, libffi-dev, zlib1g-dev.

    sudo apt install build-essential checkinstall
    sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
    

Thereafter, change directory (`cd`) to your `opt` folder \[or any convenient folder\] and download the python source code from python's server:

### First change directory (cd) to the 'opt' folder:

    cd /opt/
    

### Download the source code

    sudo wget https://www.python.org/ftp/python/3.8.3/Python-3.8.3.tgz
    

### Extract the \[downloaded\] source code files

    sudo tar xzf Python-3.8.3.tgz
    

### Change directory (`cd`) the Python Folder \[created after the extraction\]

    cd Python-3.8.3
    

### Compile the source code

    sudo ./configure --enable-optimizations
    

then

    sudo make altinstall
    

Once the compilation is completed, you can confirm that Python 3.8 has been installed successfully with:

    python3.8 -V
    

You should see the response `Python-3.8.3`.

However, to precisely answer your question, python 3.8 isn't available via ubuntu official repos. You would have to add a PPA to get python 3.8 using `sudo apt install [python3.x.x]`.

The process is described on [How to Install Python 3.8 on Ubuntu 18.04 | Linuxize](https://linuxize.com/post/how-to-install-python-3-8-on-ubuntu-18-04/)

Hope this helps and I hope I answered your question adequately.


[Source](https://askubuntu.com/questions/1261775/why-i-cant-install-python-3-8)
