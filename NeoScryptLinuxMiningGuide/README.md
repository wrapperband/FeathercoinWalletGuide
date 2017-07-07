<span id="anchor"></span>NeoScrypt Mining Guide for Linux Systems

<span id="anchor-1"></span>1. Prerequisites
===========================================

First of all, know which distribution you are using. This howto is
designed to provide information for the following Linux distributions:

Ubuntu and its derivatives including Xubuntu, Kubuntu, Lubuntu and Linux
Mint

Debian and its derivatives

Gentoo and its derivatives

OpenSuse and its derivatives \[in progress\]

Fedora and its derivatives \[in progress\]

Arch and its derivatives \[in progress\]

In this howto you will have to execute some commands. The commands are
written in blue and always start with a \# to indicate that they are
codes. While issuing commands, write the commands without the “\#”. You
can copy and paste almost all of the commands (without the “\#”) using
right click context menu as they are here. Some commands that refer to a
location (a path to a folder), of course, need to be modified before
entering. Also, you can highlight the code and paste it anywhere using
middle click.

The second step is to update your system. To achieve this, login as
root. Logging in as root, you will be able to install system-wide
programs and drivers. To login as root, open a terminal (for example a
program like Konsole in KDE or Gnome-terminal in Gnome):

and type the following command (without the \#, of course) and press
Enter:

\# su -

It will ask you for the root password. Type it and press Enter. If you
do not know the root password, you can simply change it by executing the
following command:

\# sudo passwd root

It will ask you to first enter *your own password* and after that you
can set your desired password for root.

Another way to access a terminal is that you could just press
Ctrl+Alt+F1. It will bring a console in which you can login as root and
do all of commands. Remember that you can come back to your desktop by
pressing Ctrl+Alt+F7.

Now, execute the following commands to update your system:

For Debian-based and Ubuntu-based distributions:

*\# apt-get update && apt-get upgrade*

*For Gentoo and its derivatives*

*\# emerge -uDNa --with-bdeps y --keep-going y @world @system*

Now, decide whether you want to go CPU mining or GPU mining or both.
NeoScrypt supports both types.

<span id="anchor-2"></span>2. GPU mining
========================================

**You will use you graphics card to mine* *NeoScrypt based coins such
as* *Feathercoin.**

<span id="anchor-3"></span>2.1. Using an AMD card
-------------------------------------------------

If you own an AMD GPU, First, you must have the correct drivers for your
card. Install proprietary AMD drivers for your distribution:

Ubuntu

\# apt-get update

\# apt-get install linux-headers-generic fglrx fglrx-amdcccle

Debian

\# deb http://http.debian.net/debian/ wheezy main contrib non-free

\# aptitude update

\# aptitude -r install linux-headers-\$(uname -r|sed
's,\[\^-\]\*-\[\^-\]\*-,,') fglrx-driver

Gentoo

\# emerge -na ati-drivers

\# eselect opengl set ati

\# *gpasswd -a YourUserAccount video*

After you install the driver and before you reboot, execute the
following command. This is independent of distribution. It will set up
*all* of the GPUs installed in your system.

\# aticonfig -f --adapter=all --initial

Then, reboot and check if it is correctly installed by issuing the
following command as a normal user (i.e. not as root):

<span id="anchor-4"></span>\# fglrxinfo

It should display correct information about your graphics card, for
example for an R9 290:

<span id="anchor-5"></span>2.2. Using an NVIDIA card
----------------------------------------------------

Install the proprietary driver by doing the following as root:

Ubuntu

First, run these commands:

\# apt-get --purge remove xserver-xorg-video-nouveau

\# ubuntu-drivers devices

And then from the list, choose the one that is marked “recommended”.
Most of the time, for a modern GPU this would lead to:

\# apt-get install nvidia-331

Debian

\# apt-get --purge remove xserver-xorg-video-nouveau

\# deb http://http.debian.net/debian/ wheezy-backports main contrib
non-free

<span id="anchor-6"></span>\# aptitude install linux-headers-\$(uname
-r|sed 's,\[\^-\]\*-\[\^-\]\*-,,')

\# aptitude -t wheezy-backports -r install nvidia-kernel-dkms

Gentoo

\# emerge -na nvidia-drivers

\# *gpasswd -a YourUserAccount video*

\# *eselect opengl set nvidia*

*\# eselect opencl set nvidia*

Do not miss anything. Then, do the following which is independent of the
distribution:

\# nvidia-xconfig −a −−force-generate

Once finished, restart the system. To check the installation, you should
find a program in the menu named “nvidia-settings”. As a normal user run
it and check it. It should report correct information about your
graphics card.

<span id="anchor-7"></span>2.3. Installing necessary tools for compiling the miner
----------------------------------------------------------------------------------

Debian and Ubuntu:

\# apt-get install build-essential checkinstall libssl-dev \\

libdb5.1-dev libdb5.1++-dev libboost-all-dev libncurses-dev \\

libcurl4-openssl-dev libjansson-dev git

Gentoo

\# emerge -na dev-libs/openssl sys-libs/db dev-util/boost-build
dev-libs/boost \\

sys-libs/ncurses dev-libs/jansson dev-vcs/git

Note that the backslashes make lines written above be interpreted in the
terminal as a one-line code. There should be no white spaces after the
backslashes.

<span id="anchor-8"></span>2.4. Compiling the latest Neo-gpuminer from source
-----------------------------------------------------------------------------

Neo-scrypt is developing rapidly, so the best option is to build it from
the latest available source code. You do not have to continue doing the
following as root. Log out of root:

\# exit

Or from the root terminal log into the system using your normal user
account:

\# su – youraccountname

Of course, replace youraccountname with your real account name, e.g.
john, etc. Then, get the latest code by executing the following command:

\# git clone <https://github.com/vehre/neo-gpuminer/>

Change to the downloaded directory, i.e. to neo-gpuminer

\# cd neo-gpuminer

run

\# CFLAGS="-O2 -march=native -pipe" ./autogen.sh

It will set up the package for good optimization. It should provide
results like this:

As you can see in the picture, the output indicates that it has not
found ADL/NVML. This is not good because the miner will not be able to
monitor some GPU parameters like its temperature. If you own an Nvidia
card and you have correctly installed its driver, the support for NVML
should already be found. However, for an AMD card you need to do another
step. Go to the following URL and download the latest package:

<http://developer.amd.com/tools-and-sdks/graphics-development/display-library-adl-sdk/>

Extract the zip file. You can right-click on it and using the context
menu unpack the package. Or you can use the following commands in a
terminal cd'ed to the folder where you downloaded the file:

\# cd /the/path/totheADLpackage

\# unzip -d adlpackage ADL\_\*

Then, look into the extracted package and copy the three files inside
the folder “include” to the folder “ADL\_SDK” inside neo-gpuminer
folder. You can do this in a terminal too:

\# cp /the/path/to/adlpackage/include/\*
/the/path/to/neo-gpuminer/ADL\_SDK/

If you do not know where you are and what the path is, you can find
yourself by:

\# pwd

Next, rerun the autogen.sh command above and this should be the result:

Pay attention to the other options that should be enabled. Then, issue:

\# make -jN

Replace N with the total number of your CPU cores plus 1. For example,
for a Core i7 CPU, N would be 9. This is not very important but it will
speed up the compilation process. Once finished, there should be no
error at the end of the building process:

Congratulations! You have just built the Neo-scrypt GPU miner for your
system. If you want it to be system-wide available, login as root,
change to that directory and run “make install”:

\# su -

\# cd /path/of/neo-gpuminer

\# make install

If you did not do this step, to run the program you would always have to
change to this directory and run the program like this:

\# ./cgminer --neoscrypt &lt;and the rest of the options&gt;

But when you install it system-wide, the command “cgminer” would be
recognizable from everywhere and without “./”.

<span id="anchor-9"></span>2.5. Compiling and building a Feathercoin wallet
---------------------------------------------------------------------------

Before you start mining, you must have a wallet for your coins. We are
going to download and build the wallet from source again. You could also
find a pre-compiled, binary package but that might not available for
your distribution yet.

Open a terminal and login as root (by su -). Then, install the needed
packages using the following command:

Ubuntu and Debian:

\# apt-get install libqtgui4 libminiupnpc-dev qrencode libqrencode-dev
\\

qt4-qmake libqt4-dev build-essential checkinstall libssl-dev \\

libdb5.1-dev libdb5.1++-dev libboost-all-dev libncurses-dev \\

libcurl4-openssl-dev libjansson-dev git

Gentoo

\# USE=”threads -bindist” emerge -na dev-libs/boost dev-libs/openssl:0
\\

media-gfx/qrencode \\

net-libs/miniupnpc sys-libs/db dev-qt/qtgui:4 dev-qt/qtdbus:4 \\

dev-util/boost-build sys-libs/ncurses dev-libs/jansson dev-vcs/git

Open a terminal and as a normal user (i.e. not as root) execute the
following:

\# git clone <https://github.com/FeatherCoin/Feathercoin>

Change to Feathercoin directory:

\# cd Feathercoin

Then, execute the following command:

\# qmake && make -jN

Where N refers to the number of CPU cores plus 1.

When it successfully finishes, it will make a binary file named
feathercoin-qt. You do not need to execute this program in a terminal.
Just double click on it to open your Feathercoin wallet!

<span id="anchor-10"></span>2.6. Using Neo-gpuminer
---------------------------------------------------

First, you need to create an address in your wallet. Open feathercoin-qt
(which was built in the last stage) and let it sync itself. Then, click
on “New Address” to create a valid Feathercoin address. You do not have
to write it or memorize it; you can right click on the newly created
address and choose “copy”. You can give this address to the others so
that they can send you coins. Note that not only for receiving coins a
wallet address can be used, but also it can be your user name while
doing GPU mining in some pools (mainly p2pool types). For example,
suppose that your FTC address is “9sJng4tMOUaKvs8nWoeo1b8soaivmhL6fh”,
you open a terminal and execute the following commands as a normal user
to do mining:

\# export GPU\_MAX\_ALLOC\_PERCENT=100

\# export GPU\_USE\_SYNC\_OBJECTS=1

\# cgminer --neoscrypt -o
[****http://p2pool.neoscrypt.de:19327****](http://p2pool.neoscrypt.de:19327/)
-O \\

9sJng4tMOUaKvs8nWoeo1b8soaivmhL6fh:x

The first two commands are necessary. About the last command above, you
can see that there is an “:x” after the FTC address which is a password
to be sent to the pool
[*****http://p2pool.neoscrypt.de:19327*****](http://p2pool.neoscrypt.de:19327/)****.**
**The pool simply is a group of miners who are collaborating and sharing
work to** **effectively** **find** **more** **coins sooner than the
others who are solo mining. In the command, the password “x” is not
important and can be replaced with any strings.** **Please note that
uppercase and lowercase letters would make a difference so be careful
while entering the command.** **The line written above demonstrates the
most basic code to start mining and usually users include other options
to** **tweak the** **performance. For now, just replace the FTC address
with your own and see what the result** **is. The system would start
mining and the output would be similar to** **picture 8.** **Once you
cherished it enough, press “q” or Ctrl+c to stop the program for
now.****

****Although you can go solo mining, for getting the best result, you
had better stay with a pool. The pool stated above inside the command
can be used and, of course, you can find other FTC pools, for
example**** [**http://give-me-coins.com**](http://give-me-coins.com/)
****,**** [**http://wemineftc.com**](http://wemineftc.com/) ****and****
[**http://ftc.nut2pools.com**](http://ftc.nut2pools.com/) ****.** **If
you want to connect to these pools, first you have to create an
account** **on their website. After you have created an account, in the
account setting you should change the payout address to your FTC
address. Furthermore, you have to create a worker. Creating a worker is
easy.** **Please refer to picture 9.****

As you can see above, a worker and its password have been created. This
password does not need to be very secure, although the password for your
main account should be. Suppose that you have created a worker named
“john.1” in [www.wemineftc.com](http://www.wemineftc.com/) and its
password is “x”, the command for Neo-gpuminer would be like this:

\# export GPU\_MAX\_ALLOC\_PERCENT=100

\# export GPU\_USE\_SYNC\_OBJECTS=1

\# cgminer --neoscrypt -o stratum+tcp://stratum.wemineftc.com:4444 -O
john.1:x

As you can see, the address of the pool mining server is different than
the address of the pool website. You can easily find the address of the
pool server itself for each pool on their website. For convenience, for
the three mentioned pools you might refer to the table below.

Table : Three FTC pools with their server addresses

<span id="anchor-11"></span>2.7. Tuning Neo-gpuminer
----------------------------------------------------

****In this section, we** **are going to** **speak about some parameters
that can be passed to cgminer for better performance** **and better
management.** **Your ultimate goal is to get the highest hashrate
possible with minimum hardware error. These two** **quantities** **are
marked in picture** **8.****

### <span id="anchor-12"></span>2.7.1. Parameters related to GPU health

****The first parameters that should be discussed are related to GPU
health. Since mining produces a lot of heat in the GPU, you had better
take the necessary precautions to avoid damage to** **your probably
expensive** **GPU.****

****The** **recommended** **parameters** **with examples** **are:****

****--auto-gpu :** **Bring the GPU to auto mode (always include
this)****

--temp-target 88 : The miner will try to keep the GPU temperature at
this value

--temp-overheat 91 : The miner will throttle down the GPU at this
temperature

****--temp-hysteresis 1 :** **The sensitivity of the miner program to
temperature changes** **is 1 degree of Celsius****

****--temp-cutoff 93 :** **The miner will shut down mining at this**
**temperature****

****--auto-fan: It will manipulate the GPU fan to maintain the target
temperature****

****--gpu-fan** **30-85: The program will manipulate the GPU fan in the
range of 30% to 85%****

Please note that for a multi-gpu setup (e.g. for a GPU like AMD 5970)
you can specify different values for each card. For example, in a system
with 3 cards installed:

*****--temp-target 75,80,86 : Try to keep the first card at 75 degrees,
the second at 80 and the third at 86 degrees of Celsius.*****

*****--gpu-fan 30-85,30-100,30-100 : Try to manipulate the first GPU fan
in the range of 30% to 85%, but for the second and the third GPUs it is\
allowed to crank up the fan*** ***from 30%*** ***to 100%.*****

To get the number associated with each GPU in an AMD system, run the
following command. It will display the cards' numbers with the first one
marked as “adapter 0”, the second as “adapter 1” and so forth:

\# aticonfig --adapter=all --od-getclocks

### <span id="anchor-13"></span>**2.7.2. Parameters related to performance**

The recommended parameters for a 3-card setup with examples are:

*****--auto-gpu:*** ***Set*** ***the GPUs to automatic mode***
***(always include this)*****

*****--gpu-engine 750-950,945,700-930:For the first card try to
manipulate the GPU's\
****core clock within the range of 750 MHz to 950 MHz. For\
the second card always try to keep the core clock\
exactly at 945 MHz and for the third card the allowed core clock range
is 700 to 930 MHz*****

*****--gpu-memclock 900-1250,1250,900-1150 : Like above but for the
memory clock*****

The following options are dependent on the GPU. You should manipulate
them in order to find the optimum point. Sometimes with some values the
miner program will refuse to start, or will start with errors so you
have to experiment and test different values.

*****-w 32: Set the work size to 32; can be 64, 112, 128, 256,***
***etc.*****

*****-I 14: Set the intensity to 14; can be 1 to 17 or 20*****

*****-g 2: Start 2 threads;*** ***usually it is 1 to 4*****

### <span id="anchor-14"></span>2.7.3. A complete, concrete Neo-gpuminer example

There are other non-performance related parameters that can be passed to
the program. For example, to completely hide the output you can add
*****--real-quiet*****. Another parameter called *****--no-restart*****
will be used which is a workaround for a known bug for some hardware.
Furthermore, to lower the rejected shares, pass
*****--no-submit-stale***** to the program. For more information you can
run the following command to get the complete list of options:

\# cgminer --help

****Now we want to put** **it all together.** **To achieve this, instead
of executing the commands singly,** **we want to create an executable
file named “miner” in the path /usr/local/bin** **so we will be able to
execute this single file including all the necessary commands. You can
use any text editors or** **use** **nano** **to create the file.**
**Install nano:****

Debian and Ubuntu:

\# apt-get install nano

Gentoo

****\# emerge -na** **** **nano****

****Then, as root,** **create** **the file “miner” in
/usr/local/bin/****

****\# nano /usr/local/bin/miner****

****And paste the following commands into the file:****

\#!/usr/bin/env bash

export TERM=xterm

export DISPLAY=:0

export GPU\_MAX\_ALLOC\_PERCENT=100

export GPU\_USE\_SYNC\_OBJECTS=1

load=\`aticonfig --adapter=0 --od-getclocks | grep GPU | awk '{print
\$4}'|cut -f1 -d"%"\`

if (( \$load &gt; 95 )); then

echo "cgminer was running on \`date\`"

else

echo "cgminer was not running well on \`date\`"

killall -9 cgminer

cgminer --neoscrypt --no-restart --temp-target 88 --temp-overheat 91 \\

--temp-hysteresis 1 --temp-cutoff 93 --auto-gpu \\

--gpu-engine 700-940 --****auto-fan --gpu-fan** **30-85****
--no-submit-stale \\

-o
[****http://p2pool.neoscrypt.de:19327****](http://p2pool.neoscrypt.de:19327/)
-O \\

9sJng4tMOUaKvs8nWoeo1b8soaivmhL6fh:x -I 14 -w 32 -g 1

fi

****Please note that this time the “\#”** **on the first line** **should
be included in the file. For the other commands the “\#” has already
been removed for convenience.** **For a multi-gpu setup, as you learned
before, you can set different values or use a single value for all of
them.** **** **Make the file** **executable:****

****\# chmod +x /usr/local/bin/miner****

****Please note that** **** **this** **file** **is for AMD cards**
**and, furthermore,** **you need to edit the pool address, the FTC
address and the other parameters that were** **already** **discussed.**
**As you can see** **in the script,** **the parameter**
***--gpu-memclock*** **has not been used since we did not want to change
the** **default** **memory clock of the GPU** **in this example.** **To
experiment, change the parameters and rerun the program.** **Pay
attention to the hashrate it produces and find the optimum parameters.**
**Before rerunning** **the program,** **you should** **stop** **** **the
one that is already running** **by pressing “q” or Ctrl+c.****

<span id="anchor-15"></span>****2.8.** **sgminer: an alternative mining program for AMD systems****
---------------------------------------------------------------------------------------------------

****Another program which supports NeoScrypt is sgminer. Sgminer and
Neo-gpuminer have common origins but are developed separately. Sgminer
can sometimes produce better hashrate than Neo-gpuminer so it is worth
building this program and testing it as well. Unfortunately, it does not
work for Nvidia systems so Nvidia users have to stay with Neo-gpuminer
for now.** **Another current limitation is that** **the** **program will
work only with AMD display drivers up to version 14.6\_beta2. However,
this situation and the mentioned limitation for Nvidia users might**
**change** **in the future and** **there is a good chance that these
issues have already been resolved by the time you are reading this
howto.****

****To build the program, first install the necessary packages explained
in part 2.3 and then download the software:****

****\#** **git clone****
[****https://github.com/sgminer-dev/sgminer****](https://github.com/sgminer-dev/sgminer)

****At this time you should copy** **the header files** **** **from
ADL\_SDK.zip package** **into** **sub-folder** **ADL\_SDK inside
sgminer, as you did in part 2.4 for Neo-gpuminer.** **Then:****

****\# cd sgminer****

****\# git submodule init****

****\# git submodule update****

****\# autoreconf -i****

****\# CFLAGS="-O2 -pipe -march=native" ./configure****

****\# make -j5****

****And replace 5 in make command with the appropriate number.** **You
can install the program system-wide using “make install” as root:****

****\# make install****

****You can use sgminer exactly as you do for Neo-gpuminer, however,
there are some minor differences. The first difference is the name of
the program, of course, and how you invoke the NeoScrypt algorithm:****

****\#** **sgminer -k neoscrypt &lt;and the rest of the options&gt;****

****Second,** **for** **this program some extra performance-related
parameters should be passed,** **the** **most important of which can**
**be:****

*****--thread-concurrency 8192 :*** ***A*** ***typical*** ***value
f****or an R9 280 GPU*****

****Other parameters worth mentioning:****

*****--rawintensity 6144:*** ***to tune the intensity alternatively***
***f****or an R9 280 GPU*****

*****--lookup-gap 2: Sets GPU lookup gap for mining; can be 1 or 2*****

****Again you have to play with these parameters for finding the optimum
performance.****

<span id="anchor-16"></span>**3. CPU mining**
=============================================

****There is a miner designed for CPU mining of NeoScrypt-based coins
and it is called cpuminer-neoscrypt.****

<span id="anchor-17"></span>**3.1. Installing required packages to build cpuminer-neoscrypt**
---------------------------------------------------------------------------------------------

Debian and Ubuntu:

\# apt-get install build-essential checkinstall libssl-dev
libncurses-dev \\

libcurl4-openssl-dev libjansson-dev git

Gentoo

\# emerge -na sys-libs/ncurses dev-libs/jansson dev-vcs/git

<span id="anchor-18"></span>3.2. Compiling and installing the latest cpuminer-neoscrypt
---------------------------------------------------------------------------------------

As your normal user, open a terminal and issue the following:

****\#** **git clone****
[****https://github.com/ghostlander/cpuminer-neoscrypt****](https://github.com/ghostlander/cpuminer-neoscrypt)

\# cd cpuminer-neoscrypt

\# ./configure CFLAGS="-O3 -march=native -pipe"

It will setup the package. Then:

****\# make -jN****

****Where N should be replaced with the number of the CPU cores plus
1.** **There should be no error in the compilation process and when the
building finishes, a binary called “minerd”** **would** **be present
inside the folder. If you would like to install it system-wide,
issue:****

****\# make install****

<span id="anchor-19"></span>**3.3. Using cpuminer-neoscrypt**
-------------------------------------------------------------

****You can utilize this miner in the same way you do for
neo-gpuminer.** **This is the typical command when you use the
program:****

****\#** **minerd -a neoscrypt** **-o http://p2pool.neoscrypt.de:19327
-O** **\\6sJng4tMEUaKvs8nWoeo1b8soaivmhL1hy:x****

****You can see that you will use a pool address and your Feathercoin
address.** **Picture** **10** **shows the program in action.****

<span id="anchor-20"></span>**4. Monitoring**
=============================================

****In this section,** **we will learn some simple tricks to manage our
miner system better. If you are an avid miner (or you are going to be),
you might intend to use your Linux system for mining purposes most of
the time. Mining (either CPU or GPU) exerts pressure on the system
especially when you want to mine in higher intensities.** **And usually
in higher intensities the system itself becomes so graphically
unresponsive that using mouse and working with the desktop become a
headache. Furthermore, sometimes due to high level of the noise the
system produces (high speed** **of the GPU fan), the system is put in an
isolated** **room or** **place for convenience.** **Provided that**
**you have another PC or laptop connected to the same network, you**
**can** **monitor the mining process remotely** **without touching the
mining machine directly.****

<span id="anchor-21"></span>****

****A valuable piece of software that can help is ssh. Install it on
your mining system by** **executing the following as root:****

****Debian** **and Ubuntu****

****\# apt-get install**** openssh-server

\# /etc/init.d/ssh start

\# update-rc.d ssh enable

Gentoo

\# emerge -na net-misc/openssh

\# /etc/init.d/ssh start

\# rc-update add sshd default

If you have Windows on your other PC or laptop, you can download a
program called putty:

<http://the.earth.li/~sgtatham/putty/latest/x86/putty.zip>

In Windows command prompt you can connect to your Linux machine by:

\# putty.exe <youraccountname@ip-address-of-linux-machine>

To get the internal IP address of you Linux machine, in the Linux box
execute the following as root:

\# ifconfig | grep inet

The output would be like this:

inet addr:127.0.0.1 Mask:255.0.0.0

inet addr:192.168.1.5 Bcast:192.168.1.255 Mask:255.255.255.0

Then, in this example, the IP address of the machine is 192.168.1.5. If
your account in the Linux box is, for example, john, you can connect to
your mining machine:

\# putty.exe <john@192.168.1.5>

It would ask for your account password. Once you logged in, it would be
a Linux terminal for you. So everything you execute there, would be
executed on the Linux machine.

So far we have learned how to connect to a Linux box remotely. However,
typing commands is boring and sometimes tedious, so we want to wrap
useful monitoring commands in shortcuts. Get back to the Linux machine
(either directly or remotely) and ****as a normal user do the
following:****

****\#** **cd****

\# echo "\[\[ -f \~/.bashrc \]\] && . \~/.bashrc" &gt;&gt;
.bash\_profile

\# chmod +x .bash\_profile

Now we want to create some useful shortcuts for monitoring an AMD GPU.
If you want to get the temperature of the GPU you can execute:

\# aticonfig --adapter=all --od-gettemperature

And if you want to see the GPU load:

\# aticonfig --adapter=all --od-getclocks

Now we want to create shortcuts named “gettemp” and “getload” for these
two useful commands:

\# echo “export DISPLAY=:0” &gt;&gt; .bashrc

\# chmod +x .bashrc

\# echo "alias gettemp='\`which aticonfig\` --adapter=all
--od-gettemperature'" &gt;&gt; .bashrc

\# echo "alias getload='\`which aticonfig\` --adapter=all
--od-getclocks'" &gt;&gt; .bashrc

\# source .bashrc

Well done. Now instead of typing the whole line of the original
commands, to get the temperature and the load of the GPU, you can simply
type:

\# gettemp

\# getload

If you want other names, change “gettemp” and “getload” to whatever you
would like in the echo commands. If you did something wrong, or later
you want to change the names, you can edit the file .bashrc as your
normal user using any text editors or using nano in the terminal:

\# nano \~/.bashrc

Edit the file and once you have done editing, press Ctrl+x to save the
file and quit the program. Another useful and fun shortcut can be:

\# echo "alias killit='killall -9 cgminer'" &gt;&gt; .bashrc

So whenever you need you Linux box urgently and it is unresponsive due
to high load, get into the box through ssh and execute killit to relieve
it!

\# killit

<span id="anchor-22"></span>5. Task management
==============================================

Sometimes you want to mine only during specific times of the day. Or you
want to mine continuously, but some unexpected problems occur that
interfere with the mining process. For example, the pool becomes
unavailable or the Internet gets disconnected. In such situations if you
do not pay attention to the miner, it might become idle. We are going to
manage this through task scheduling. As root, install the following
packages:

****Debian** **and Ubuntu****

****\# apt-get install** **cron** **nano****

\# /etc/init.d/cron start

****\#** **update-rc.d** **cron** **enable****

****Gentoo****

****\# emerge -na** **** **nano sys-process/vixie-cron****

****\#**** *rc-update add vixie-cron default*

*\# /etc/init.d/vixie-cron start*

*\# gpasswd -a yourusername cron*

****Then, as your normal user** **run:****

\# export EDITOR=nano

****\# crontab -e****

****The nano text editor will come up, waiting for editing. Now you can
enter specific commands here.** **The general structure of the file is
as** **depicted in the diagram below.****

\* \* \* \* \* Command to be executed

- - - - -

| | | | |

| | | | +----- Day of week (0-7)

| | | +------- Month (1 - 12)

| | +--------- Day of month (1 - 31)

| +----------- Hour (0 - 23)

****+------------- Min (0 - 59)****

****Now we want to make examples. In the first example, you want to mine
24 hours a day, 7 days a week nonstop. So your** **mining system should
never be idle.** **Fortunately,** **in section 2.7.3** **** **we already
created an executable file named “miner”** **which** **is ready to be
utilized here, too.** **Just edit that file and append the option**
***--real-quiet*** **to cgminer command.** **Now, because we want to
make sure that cgminer is always running, the contents of the crontab
would be like this:****

****\*/3\*\*\*\*/usr/local/bin/miner****

****Copy and paste the piece of text above into the crontab. Press
Ctrl+x, say “y” and press Enter.** **As you might guess from the
command,** **** **the cron scheduler will execute the program “miner”
every 3 seconds.** **The contents of the file “miner” includes a
conditional, so it** **will** **work out the situation by itself.**
**This way, it would resist any problems** **and would try endlessly**
**unless some serious OS failure happens** **which** **is** **really
rare** **in Linux** **due to its robustness and stability. So your
system** **can mine years continuously and** **will never rest** **until
it literally dies!****

****In another example, suppose we would like to start mining when we**
**leave the house and** **go to work at 7 a.m. and we want it to
automatically stop mining when we come back home at 4** **p.m. The
contents would be like this:****

****\*/37-15\*\*\*/usr/local/bin/miner****

****116\*\*\*\`which** **killall\`** **-9 cgminer****

****You can see that cron will start the job at 7 and would kill it at**
**16:01.****

****You can simply create your own scheduler that fits your specific**
**goals.****
