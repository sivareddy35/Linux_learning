## Linux_learning:
#### Operating System(OS):
* OS is an interface between user and hardware. OS converts human readable language to binary to have a perfect communication between both human hardware.
* OS consists of:
  
      Sourcecode + applications 
      Kernel + software
      Operating System
* Source code is the base code in wchich entire software or operating system is built, what OS can and can't do. Compilers and libraries are added in applications.
* Source code and Applications combined gives `Kernel`, which is heart of OS everything in the system depends on kernel. We will give instructions to kernel to perform amny activity in OS. ALl kinds of management is handled by kernel ie file management, CPU, process and memory management..
* Software the one which is used to accept the instructions to work on. Ex music player, browser.
* OS is combination of kernel and software and kernel is combination of source code and applications.
#### History of Unix:
* Unix was introduced by Ken Thompson and Denis Ritchie in AT&T Bell Labs, introduced in 1969. By adopting unix source code many flavoures were introduced.
  
       HP          HP-UX        1984
       APPLE       Mac OS       1984
       IBM         AIX          1986    Advance Interactive Xecutive(AIX)
       SUN/ORACLE  SOLARIES     1992
* These unix's are hardware propreitarty hardware systems, they can work on the specific hardware, which makes it costly.
* Free Software Foundation (FSF) started a movement calles GNU (Generally Not Unix motive) movement.
* Linux was developed by `Linus Torvalds` in 1991.Linus is open source, hardware Independent.
* CentOS(Community Operating system) is copy of RedHat. RedHat charges for the support.
   <img width="736" height="307" alt="image" src="https://github.com/user-attachments/assets/b62d8acb-e25c-49c6-8f2a-13a59b62f0b6" />
#### Areas of where Linux is used:
* `Virtualization`:
  * It is a method of splitting the physical resources into logical or virtual.
  * It allows multiple operating system instances to run concurrently on a single computer.
  * On the top of a single physical machine with a setup of resources such as virtual CPU, memory, hard disk, network card on the top  virtualisation softwares (VmWare, VSpehere ESXI ) are installed on top ofg it will install Virutal Machines.
  * Although it it virtual in nature the VM works as independent physical machine.
  * On a single hardware we can run hundreds of Virtual machines with differnt OS in them.
  * Hypervisors: VmWare, Citrix Xan, KVm, Oracle VM, RedHat Virtualization--> all these uses RedHat kernel in the mini operating system Mirosoft Hyper-V
* `Cloud Computing`:
  * The practice of using a network of remote servers hosted on the Internet to store, mapping and process data rather than a local server or a personal computer.
  * Public clouds are Amazon Web Services, Google Cloud, Azure.
  * On-premise cloud: Openstack, Open Cloud, Redhat OpenShift, apacheCloudStack.
* `Devops`:
  * Devops is a set of practices that combines software development and IT operations.
  * Devops is the combination of a cultural philosophies, practices and tools that increases an orginization's ability toi deliver applications and services at high velocity.
     <img width="674" height="265" alt="image" src="https://github.com/user-attachments/assets/5ccc82ab-fe9e-43f0-9c17-1c4892a2afd8" />
#### Linux Architecture:
 <img width="598" height="406" alt="image" src="https://github.com/user-attachments/assets/8e032603-ca0e-4d19-80a8-9dafdbf3f42b" />
 
 * The inner most layer in which all the commands are executed are known as hardware layer. Ex: Music played will give output in the speaker, a file is created the file stored in hard disk.
 * When we search a web site through ethernet adapter (hardware) the communnication will happens.
 * On the top of hardware layer there will be `kernel` layer which controls the hardware. Kernel manages every thing managed  or performed. When we type a web site, we are giving instruction to kernel and kernel is taking you to the website. File, cpu, memory, process management...
 * Users on the top or end of the layers. Users uses some ultities and softwares to communicate with Kernel. User can understand user friendly languages but kernel works with binary codes, to communicate we will use interpreter, here the interpretter is noting but `shell`.
 * Shell is an utility that converts user friendly language to machine level language. 
 * Users access Shell, the shell is of two types one is graphical shell and another is Command Line Shell. In cli shell will check the command is correct ot not, if correct it proceed to the next step. If it is incorrect we will get error messages on the screen.
 * Based on cli command kernel perform the task in the specific hardware. The date and time configurations are stored generally in the mother board under CMos battery.
#### File system Hierarchy:
* Linux uses single rooted, iverted tree like file system hierarchy.
* `/`:
  * This is top level directory. It is parent directory for all other directories. It represented by forwarded slash(/).
  * This is called `ROOT` directory. `c:\ of windows`.
* `/root`:
  * It is home directory for root user (super user), it provides working environment for root user `c:\Documnets and Settings\Administrator`
* `/home`:
  * It is home directory for other users. It provides working environment for other users (other than root user) `c:\Documents and Settings\username`
* `/boot`: OS maintain the important bootable files.
  * It contain bootable files for linux like vmlinuz(kernel)...ntoskrnl, Inird(INITial Ram Disk), drivers.. 
 and GRUB(GRand Unified Boot Loader).... boot.ini, ntldr
* `/etc`:
  * It contains all configuration files.
  * /etc/passwd ... user info
  * /etc/resolv.conf... Preffered DNS
  * /etc/dhcp.conf ... DHCP Server
  * c:\windows\system32\drivers\
* `usr`: all OS softwares are installed
  * by default softwares are installed in /usr directory (Unix Sharebale Resources)
  * c:\program files
* `\opt`: non-os softwares are installed here
  * It is optional directory for /usr
  * It contains third party softwares
* `/bin`:
  * It contains commands used by allm users (Binary files). These are non-admin commands. ex: date, clear, cp, cat, ls ...
* `/sbin`:
  * It contains commands used by super User(root) (Super User's binary files). Networking, new software installation, shutdown the system, reboot...
* `dev`:
  * It contains device files
  * /dev/hda ... for hard disk
  * /dev/cd rom .. for cd rom
  * Similar to device manager of windows.
* `/proc`:
  * It contains process files.
  * Its contents are not permanent, they keep changing
  * It is also callad as Virtual Directory
  * Its file contain useful information used by OS
  * /proc/meminfo... information of RAM/SWAP
  * /proc/cpuinfo... information of CPU
  * task manager in windows
* `/var`:
  * It contains variable data lije mails, log files
  * Any activity we do in the system are called events, the files are stored in /var
  * All mails are stored under /var folder
  * Once if we try to login to the system with correct user name and password one event will be logged with user detals and time and if failed will also be logged. 
* `tmp`:
  * Contains temporary files for small period of time
  * Code is pushed from one machine and reached our computer once it reaches to your computer to install the code in the software. This new software is stored temporarily before installation in /tmp
* `mnt`:
  * It is default mount point for any partition.
  * It is empty by default
* `media`:
  * It contains all removable media like CD-ROM, pen drive.
  * It is mount point for removables.
* `/lib`:
  * It contains library files which are used by OS
  * It is similar to dII files of windows
  * Library files in Linux are OS(shared object) files
  * Whenever we installl some software some libraries will be installed.
    
* Config file store the information that how you want to use certain software or application and all these config files are stored under /etc.
  











  
