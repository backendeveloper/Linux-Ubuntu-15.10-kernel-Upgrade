
# Linux Ubuntu Kernel Upgrade


Install the necessary tools to compile the linux kernel

```{r, engine='bash', count_lines}
$ sudo apt-get install gcc libncurses5-dev dpkg-dev
```
And then, 

[sudo] password for USER: ENTER USER PASS

After, Download the lastest Linux Kernel Version, [this site](https://www.kernel.org/)

Enter the directory of the extracted kernel source

Configure the Kernel


```{r, engine='bash', count_lines}
~/kernel/linux-4.3$ make menuconfig
```

In this menu you can customize your kernel

![alt tag](http://i.imgur.com/pGKHvmn.png)

Save and exit

Compile the kernel

```{r, engine='bash', count_lines}
~/kernel/linux-4.3$ make-j 5 KDEB_PKGVERSION=1.YOURCUSTOMNAME deb-pkg
```

Get a cup of coffee or a beer beacuse is going to take a while:)    

After, Install the kernel

```{r, engine='bash', count_lines}
~/kernel/linux-4.3$ sudo dpkg -i ../linux*.deb
```

After that,

```{r, engine='bash', count_lines}
~/kernel/linux-4.3$ sudo reboot
```

And again, info last kernel version

```{r, engine='bash', count_lines}
~/kernel/linux-4.3$ uname -a
```

DONE :+1:

Reference Youtube Video:

[![Everything Is AWESOME](https://i.ytimg.com/vi/bSS7oJ7n6f0/hqdefault.jpg)](https://www.youtube.com/embed/bSS7oJ7n6f0 "Everything Is AWESOME")
