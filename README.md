## Compile the kernel
```
sudo apt-get install git libncurses5-dev libncursesw5-dev libelf-dev libnl-3-dev libssl-dev  
git clone https://github.com/kdkalvik/Atheros-CSI-Tool.git
cd Atheros-CSI-Tool
make menuconfig
make -j16
make modules
sudo make modules_install
sudo make install 
sudo reboot
```

##Linux kernel
This file was moved to Documentation/admin-guide/README.rst

Please notice that there are several guides for kernel developers and users.
These guides can be rendered in a number of formats, like HTML and PDF.

In order to build the documentation, use ``make htmldocs`` or
``make pdfdocs``.

There are various text files in the Documentation/ subdirectory,
several of them using the Restructured Text markup notation.
See Documentation/00-INDEX for a list of what is contained in each file.

Please read the Documentation/process/changes.rst file, as it contains the
requirements for building and running the kernel, and information about
the problems which may result by upgrading your kernel.
