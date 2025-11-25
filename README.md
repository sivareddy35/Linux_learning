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

### RHEL Installation:  
  <img width="595" height="220" alt="image" src="https://github.com/user-attachments/assets/77d2e946-ebb0-4600-bfc7-a75acb3713f0" />
  
* Oracle Virtualbox works based on KVM(Kernerl Virtual Machine)

* We need to check the minimum/recommended configuration to install RHEL7/8.
* Dual core processor is a single physical processor but logically it beahave like two. Quad Core one physical but behaves like 4 CPU.
* Processors can be of 32 bit and 64 bit based on the processor the data processing speed will change bu to work with virtualization we need to have 64 bit architecture.
* During the installation we need atleast 3 partitions. `/(root)`, `/boot`,`SWAP`.
  * `/` sould have most of the memory. Since everything starts with this root directory only.20-30 GB recommended.
  * `/boot` is immediately required at the time of booting even before root directory. 1 GB
  * `SWAP` is needed to support RAM, which should be twice of RAM approx preferred. Twice the RAM approx.
* While installing RHEL in windows we use host based hypervisor ie we need to have installed an OS on the hardware and we are installing OracleVirtual box on the top of ity we are installing Virtual Machines(VM).
* Incase of production environment full virtualization is used which is called as `Bare Metal Hypervisor` or `type1` hypervisor.
* In Bare Metal on the top of physical machine virtualization softwares like `ESXI`,`Citrix Z`,.. on the top of it VMs are created.
*  We need to have vitualization enabled in windows, we can check this from task manager --> performance --> virtualization (enable). If not enabled it will not allow to use 64 bit linux VM, only provides32 bit windows.
   <img width="834" height="445" alt="image" src="https://github.com/user-attachments/assets/9b67834b-7886-45a3-8a0b-031a3f7432c2" />
   <img width="865" height="437" alt="image" src="https://github.com/user-attachments/assets/9e3d03c7-45c6-452a-9a08-4e9e4291b59d" />


* While installing OS in windows we will change settings in bios setting the first bootable device is CD but in VM we need to open VM settings.
* Under VM settings open processor update the processor to 2 core and under mother board there wil be boot order available ie floppy, CD, HardDisk, Network. Change the order Optical< HArd Disk, Network.
* Update the pointing Device from the mother board to USB Tablet or USB multi Touch Tablet.
* We will share ISO image instead of DVD from storage section and upload ISO image by selecting DVD option.
* We can use mouse by clicking on the VM screen, the mouse to come out of VM use right hand side `ctrl` key to work with computer.
* Anaconda is an installer with the help of which we install RHEL.
  
   <img width="855" height="438" alt="image" src="https://github.com/user-attachments/assets/cded11e5-90b1-4771-a6c8-32bc196d2b3f" />
   <img width="940" height="398" alt="image" src="https://github.com/user-attachments/assets/25be02fe-b3be-44f4-88ab-21052976f67f" />

* Installation destination is the partition where the OS need to be installed, storage configuration (auto / custom). If auto is selected entire allocated 30GB will be devided into default partition. We will have standard / LVM partition.
* Select standard and click `+` to make partitions, add `/` with required in `G`(GB), `/boot` and `swap` partitions.
* KDUMP is a kenrel crash dumping mechanism, in the event of system crash, it capture the information from your system that can be invaluable in determining the cause of crash. It need a portion systems memory to reseve that is not avaible for other users. It should be allowed memory auto allocation
* Networking--> provide a name, select some ethernet adaptor and config -->under general --> connect automatically (If we don't select the system will bppt every time the adaptor will be down).
* Under IPVersion4 settings --> Automatic (DHCP) by default but we can change it by selecting manual option and provide an IP like 198.168.10.70 and press `tab` key Netmnask will be selected and save.
* Click on ON beside the Ethernet (enpox3). it will provide an ip.4
* From the start of the VM file option we need to change host netork manager, in the ptoperties section change IPv4 adrress in the same range of VM and save.
* Once again open setting of VM and network and change to hostonly option after some time ping -t <vm_ip> can be connected.
* Change root password to the required and reboot the VM.

#### Linux basic commands:
* On a professional network we will be having VPN from client to server we have to connect with VPN and the seerver network/ datacenter network will be accessed there after.
* To connect from local with server IP we will use some softwares like putty/ Mobaxterm/ sshCleient,..
  
      ping -t <server_ip>   checks if the server is up and running or not.
      whoami    Loggedin user name
      pwd       print working diredtory
      ctrl + d  exit the session
      date      print today's date
      cal       print calender
      ls        print all files/ directories
      ls -l     print the filee/ directories in long format
      ls -l <file_name>   print properties of the file
      ls -ld  <file_name>  print properties of the directory
      cd ..     to gho back one step back in the server cli
      ls <directory_name> diplays the files inside the directory
      cd <directory>     to login to the directory.
  
      nsivareddy@X-J3PVH32KM4 ~ % ls -l
      total 6
      -rw-r--r--@  1 nsivareddy  staff     7191  7 Oct 21:50 automated_cert_renewal.sh
      drwxr-xr-x   4 nsivareddy  staff      128 21 Oct 06:00 bin

* The name of the file will be black color but folder will be in blue color.
* If a file starts with `-` while directory starts with `d`.
* `drwxr-xr-x` are file /folder permissions & `4` is called as links.
* `nsivareddy` is user and  `staff` is group.
* `7191` is size of the file and `7 Oct 21:50` file or folder creation date.
##### Create a file in Linux:
* `cat`(Concatenate) command is used to create a file and to display and modify the contents of a file.
  
        cat > filename(say myfile)
        hello world
  * crtl + d (to save the file). If we have existing file with the same name `cat` command `replace the existing` and if thre is no file it will create a new file.
  * We can go to above lines one we enter to the next lines.
    
        nsivareddy@X-J3PVH32KM4 ~ % cat > myfile
        hello world 
        ^C
        nsivareddy@X-J3PVH32KM4 ~ % cat myfile 
        hello world
* `cat -n filename` it will diplays the file with numbers in each line but these numbers are not saved.
* `touch` command creates an empty file. When we recreate a file or directory it won't change the exiting but if not exits it create file/ directory.
* If want to create multiple empty files.
  touch <file_name> <file_name> <file_name>
  touch file1 file2 file3
  touch file{1..100}  create files wilth file1, file2,.. file100
#### Creating a Directory:
* `mkdir <file name

       mkdir mydir        mydir directory is created
       mkdir d1 d2 d3     multiple directories are created
       mkdir mydir{1..5}  multiple directories with the range will be created
       cd .. / ..         to go back to two steps back
       cd                 will bring to root(`/`) directory
       cd -               will bring back to the last opended directory
  
* If we try to create a directory with the same name it will through error that `directory exists`. mkdir won't override.

      X-J3PVH32KM4:~ root# mkdir mydir
      X-J3PVH32KM4:~ root# cd mydir/
      X-J3PVH32KM4:mydir root# mkdir mydir{1..5}
      X-J3PVH32KM4:mydir root# ls
      mydir1	mydir2	mydir3	mydir4	mydir5
      X-J3PVH32KM4:mydir root# pwd     
      /var/root/mydir
      X-J3PVH32KM4:mydir root# cd mydir1
      X-J3PVH32KM4:mydir1 root# pwd
      /var/root/mydir/mydir1
    
* Absoulyte path is the complete path from `/`(root) directory.
* To moveforward to multiple directories in forward we need to use `cd mydir/mydir1`. Use Tab key to open the next directory and proceed.
* `mkdir -p main/sub` this will create a sub directory in main directory, here `p` stands for parent directory. If main directory already existing i will not do anything for main but creates a child directory `sub`.
* `mkdir -p main/sub2` it will create a `sub2` directory inside the existing main directory.
* `mkdir -p park/{table,bench,trees}` it will create `lion`, `leopard` and `tiger` sub directories with in main directory.

      X-J3PVH32KM4:~ root# mkdir -p park/{table,bench,trees}
      X-J3PVH32KM4:~ root# cd park/
      X-J3PVH32KM4:park root# ls
      bench	table	trees
* To create directories inside directories.
  
      X-J3PVH32KM4:~ root# mkdir -p world/{IND/{BANG,HYD},AUS/{SYD>MEL},USA/{NY,NJ}}
      X-J3PVH32KM4:~ root# ls world/
      AUS	IND	USA
      X-J3PVH32KM4:~ root# cd world/
      X-J3PVH32KM4:world root# ls IND/
      BANG	HYD
      X-J3PVH32KM4:world root# ls AUS/
      MEL	SYD
      X-J3PVH32KM4:world root# ls USA/
      NJ	NY
* `tree world` View the directory in tree form

      X-J3PVH32KM4:~ root# tree world/
      world/
      |-- AUS
      |   |-- MEL
      |   `-- SYD
      |-- IND
      |   |-- BANG
      |   `-- HYD
      `-- USA
          |-- NJ
          `-- NY

      10 directories, 0 files
* `ls -R world` recurssive/iterate displays the all the subdirectories in the main directory.

        X-J3PVH32KM4:~ root# ls -R world/
        AUS	IND	USA
        
        world/AUS:
        MEL	SYD
        
        world/AUS/MEL:
        
        world/AUS/SYD:
        
        world/IND:
        BANG	HYD
        
        world/IND/BANG:
        
        world/IND/HYD:
        
        world/USA:
        NJ	NY
        
        world/USA/NJ:
        
        world/USA/NY:
#### Copying files to a directory:
* `cp <source> <destination directory in which to paste the file>` copy a file from one location to destination directory
* `cp file1, file2, file3 main` copies file1,file2 and file3 to main directory.
* `cp file{1,2,3} main` if there are files in a sequential name.

        X-J3PVH32KM4:~ root# cp file1 main
        X-J3PVH32KM4:~ root# ls main/
        file1
* If there is existing file in the same directory it will ask if it need to over rider with `y` option to proceed to replace or `n` to abort.

#### Copying a directory to anothe directory:
* we need to use `-r` while copying directory mandatorily. 
* `-v` verbose display what is copiing
* `-f` copy the data forcefully
* `-p` to preserve the permissions and and paste.
  
       cp -r main zoo         copies main directory to zoo directory
       cp -r 1 2 3 main       copies 1,2,3 directories to main directory
#### Move file from one location to another (cut and paste):
* It will cut the original file completely and put in some other location
* `mv <filename> <Destination Directory>`
* `mv myfile mydir`   Move file1 to mydir directory.
* `mv dir1 newdir`  it will cut the directory from source to destination directory, no need to use `-r` flag.
* `-i` interactive mode which prompts beore overwriting.

        X-J3PVH32KM4:~ root# ls
        .CFUserTextEncoding	Library			main			tiger,
        .bash_history		file1			mydir			world
        .forward		leopard}		park			zoo
   
        X-J3PVH32KM4:~ root# mv file1 mydir/
        X-J3PVH32KM4:~ root# ls
        .CFUserTextEncoding	Library			mydir			world
        .bash_history		leopard}		park			zoo
        .forward		main			tiger,
   
        X-J3PVH32KM4:~ root# ls mydir/
        file1	mydir1	mydir2	mydir3	mydir4	mydir5
* To rename also we will use `mv` command it self.
* mv <curent name> <new name>
* In the background it is copying the file contents to new file i ebn through it is rename the file.
* If the new name which we want to change exists then it moves the content, if not exists it will rename the file.

#### Removinga file:
* `rm filename` or `rm -f filename`(without prompting)
* Unlike in windowds recyle bin there is no directory to restore the deleted files/directories.
* To delete multiple files use `rm -rf file1 file2` 

        X-J3PVH32KM4:~ root# rm file1
        X-J3PVH32KM4:~ root# ls   
        .CFUserTextEncoding	Library			mydir			world
        .bash_history		file2			park			zoo
        .forward		main			tiger,
#### Remove directory:
* `rmdir directoryName` removed the directory.
*  We can't delete non empty directory with `rmdir` command need to remove the directories with in the main directory and delete main directory at last.
* use `rmdir -rf directory` to remove directory recurssively.
  
        X-J3PVH32KM4:~ root# rmdir zoo/
        rmdir: zoo/: Directory not empty
        X-J3PVH32KM4:~ root# rm -rf zoo
        X-J3PVH32KM4:~ root# ls
        .CFUserTextEncoding	.forward		main			park			world
        .bash_history		Library			mydir			tiger,
  
* If we want to delete all files or directories use `rm -rf *`, here `*` means all.
        X-J3PVH32KM4:test root# ls
        dir1	dir2	dir4	dir6	dir8	file1	file2	file4	file6	file8
        dir10	dir3	dir5	dir7	dir9	file10	file3	file5	file7	file9
        X-J3PVH32KM4:test root# rm -rf *
        X-J3PVH32KM4:test root# ls
        X-J3PVH32KM4:test root# 
* If we want to delete files in side a particular directory use `rm -rf main/*`
* `mv mydir/file1 root`  movee file1 to root directory
* `mv mydir/file1 .`  move the file to current directory `.` is curent location

        poweroff --> shutdown the machine
        reboot   --> reboot the machine
### VIM Editor:
* Vim is command mosde editor for files, other editors in Linux are emacs, nano and gefit.
* Vim has 3 modes: Command Mode, Insert mode(edit mode), extented command mode.
* When you open the vim editor, it will be in the command mode by default.
* In command mode the cursor's can be used as `h/l/k/j` to move `left/right/up/down
* We can create a file and edict a file. If there is no file with that name it will create a file open in edit mode but if the file exiting it open the file in edit mode.
  
* **Insert Mode**:
  
        i to bring insert mode at the cursor position
        I to insert at the begining of the line
        a to append to the next word's letter
        A to appenf at the end of the line
        o to insert new line below the cursor position
        O to insert a new line above the cursor position
  
* `vi filename`, it will open in read only mode, if we want to modify/ update the file press `i`(insert) mode and to save `esc+:!wqa` save and exit.
* If we don't want to save changes and exit `esc+ q!`
* **Command Mode**:
  
        gg    to go to the beginning of the line
        G     to go to the end of the file
        w     to move the cursor forard, word by word
        b     to move the cursor backward, word by word
        nw    to move the cursor forward to n words(5W)
        u     to undo last change (word)
        U     to undo the previous change (entire line)
        Ctrl + R to redo changes
        yy    to copy a line (y is yanking)
        nyy   to copy n lines(5yy or 4yy)
        p     to paste line below the cursor position
        P     to paste line above the cursor position.
        dw    to delete word letter by letter (like Backspace)
        x     to delete the word letter by letter (like Del key)
        dd    to delete entire line
        ndd   to delete n no.of lines from cursor position(5dd)
        /      to search a qord in the file but it is case sensitive 
  * If want to delete anyline use `dd` and don't use `p` or `P`, after `dd` command if we use `p` or `P` it will paste the lines deleted.
  * `/` and type a word you want to search but it is case sensitive and to move to the next matching word need to press `n` to go to sequence of searches.
* `Extended Mode:(Colon Mode)`:
* Extended mode is used for save and quit or save without quit using `Esc`key with `:`.
* We can move to a specific line number with `Esc+:10` the cursor will move to the start of line number 10 and if we search the more than the available lines in the file the cursor move to the start of the last line.

        Esc+:w       To save the changes but still in the editor
        Esc+:q       To quit (without saving)
        Esc+:wq      To save and quit
        Esc+wq!      To save and quit forcefully
        Esc+x        To save and quit
        Esc+X        To give password to the file and remove password, data is encrypted. There is no way to recover password
        Esc+:20(n)   To go to line no 20 or n
        Esc+:se nu    To set the line numbers to the file
        Esc+:se nonu  To Remove the set line numbers
* Once we save a file with `Esc+X` encryption there is no way to recover it and we can remove the password after login `Esc+X` and don't enter password (just enter + enter).

        nsivareddy@X-J3PVH32KM4 practice % vi test.txt 
        nsivareddy@X-J3PVH32KM4 practice % cat test.txt 
        VimCrypt~03!O?_???????g#vs@??
        ])?c?݌l"??>_?????2?F???}9k`vf???^Ù????O?p?.~ּ[
                                                     /ޱ????~쌜X?:Jc{?C??sy???oHD?J?#????ݽZ??}???<?????5v??'??P?|
                                                                                                                ?F?Ѽ?K6䢊ʫC=
        Bf?{P?????t????*|????e}<?4[?????G?G?j?A?%                                                                                                     nsivareddy@X-J3PVH32KM4 practice % 

* To open multiple files in vim editor
  
      vim -o file1 file2
    * To switch between files use `Ctl+w`.
* `vim -o file1 file2` this open an editor with the two files witin the same editor.
* This wil be helpful when we want to compare and want to copy some lines from one to another. By pressing `Ctl+w` twice we can switch these two files and do copy and paste.
* We can save the files `Esc+wq!` if we are copying file from 1st to second, `Esc+wq!` will save second file first and next first file will be saved.
#### Listing files and directories

      #ls          list with filenames
      #ls -l       long listing of the file
      #ls -l       filename to see the permissions of a particular file
      #ls -al      shows the files in ascendeing order of modification
      #ls p*       All the files start with p

#### Types of Files:

    Symbol     type of file
      -            Normal file
      d            Directory
      l            Link file(shortcut)
      b            Block file(Harddisk, Floppy disk)
      c            Character file(Keyboard, Mouse)
* Unix/ Linux stores every thing in the form of file i.e sofrtware, hardware, directory and file is also a file.

      nsivareddy@X-J3PVH32KM4 ~ % ls -l /
      total 13
      drwxrwxr-x  33 root  admin  1056 22 Nov 00:39 Applications
      drwxr-xr-x@ 39 root  wheel  1248 17 Aug 00:14 bin
      drwxr-xr-x   2 root  wheel    64 12 Jan  2024 cores
      dr-xr-xr-x   4 root  wheel  6508 31 Oct 03:46 dev
      lrwxr-xr-x@  1 root  wheel    11 17 Aug 00:14 etc -> private/etc
      lrwxr-xr-x   1 root  wheel    25 31 Oct 03:46 home -> /System/Volumes/Data/home
      drwxr-xr-x  71 root  wheel  2272  7 Sep 23:51 Library
      drwxr-xr-x   4 root  wheel   128 21 Oct 22:36 opt
      drwxr-xr-x   6 root  wheel   192 31 Oct 03:46 private
      drwxr-xr-x@ 76 root  wheel  2432 17 Aug 00:14 sbin
      drwxr-xr-x@ 10 root  wheel   320 17 Aug 00:14 System
      lrwxr-xr-x@  1 root  wheel    11 17 Aug 00:14 tmp -> private/tmp
      drwxr-xr-x   7 root  admin   224  7 Sep 23:50 Users
      drwxr-xr-x@ 11 root  wheel   352 17 Aug 00:14 usr
      lrwxr-xr-x@  1 root  wheel    11 17 Aug 00:14 var -> private/var
      drwxr-xr-x   4 root  wheel   128 21 Nov 00:10 Volumes
* `ls -l \dev\sda` here `/sda` is hard diskfile which can't be readable.
* `cat \dev\sda` is not readable and is protected by kernel operating system.
* `cat \dev\tty0` is printer device
  
   <img width="597" height="99" alt="image" src="https://github.com/user-attachments/assets/bb97d9d4-ccc1-453b-8247-00d560338b70" />

#### Symbolic links:

