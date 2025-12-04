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

#### Copying a directory to another directory:
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
  
      
* `ls -ld *` list all files and directories in a long format witout entering directories.
* Ex:
      mkdir dir1 dir2
      touch file1.txt file2.txt
  
      # Run the command
      ls -ld *
      drwxr-xr-x 2 user group 4096 Nov 26 10:30 dir1
      drwxr-xr-x 2 user group 4096 Nov 26 10:30 dir2
      -rw-r--r-- 1 user group    0 Nov 26 10:30 file1.txt
      -rw-r--r-- 1 user group    0 Nov 26 10:30 file2.txt
* `ls -ld */` lists only directories in long format.
  
      ls -ld */
      drwxr-xr-x 2 user group 4096 Nov 26 10:30 dir1/
      drwxr-xr-x 2 user group 4096 Nov 26 10:30 dir2/
* `ls -ld directory_name` Shows information about the directory itself(not its contents)
* Ex:
      mkdir myproject
      touch myproject/file1.txt myproject/file2.txt
      
      # WITHOUT -d flag (shows directory contents)
      ls -l myproject
      #Output:
      -rw-r--r-- 1 user group 0 Nov 26 10:30 file1.txt
      -rw-r--r-- 1 user group 0 Nov 26 10:30 file2.txt
  
      # With -d flag(shows directory info)
      ls -ld myproject
      #output:
      drwxr-xr-x 2 user group 4096 Nov 26 10:30 myproject
 * `ls -l myproject` shows the files inside the directory.
 * `ls -ld myproject` shows directiry as an entry
    
* `ls ? ample`  matches files with exactly One character before "ample"here `?` exactly one character(any character). Total: 6 characters(X + ample).
 * Ex:
      nsivareddy@X-J3PVH32KM4 practice % touch sample example xample 1ample ample
      nsivareddy@X-J3PVH32KM4 practice % ls ?ample
      1ample	sample	xample
* `ls [ae]` list all the files starting with `a` or `e` followed by anyting (or nothing). ie first character must be `a` or `e`. `*` followwd by zero or more characters.
 * ex: 
      nsivareddy@X-J3PVH32KM4 practice % touch apple.xt ample example.txt banana.txt elephent.txt file.txt
      nsivareddy@X-J3PVH32KM4 practice % ls [ae]*
      ample		apple.xt	elephent.txt	example

* `ls [aeiou]*` files starting with vowels.
* `ls [0-9]*` files starting with numbers.
* `ls [A-Z]*` files starting with uppercase letters.
* `ls [!ae]*` list files NOT starting with `a` or `e`. First character must NOT be `a` or `e`. `*` followed by zero or more characters.
ls [!]

      ls '[!ae]' or ls [\!ae]* or ls "[\\!ae]" files must NOT start with a or e letters
      ls [!aeiou]*     file must NOT starting with vowels.
      ls [!0-9]*       files must NOT start with numbers
      ls [!a-z]*       files must NOT start with letters
      ls [a-zA-Z]*     file start with lower and upper case letter

* `ls [am][c-z][4-9]` Matches file with exactly 3 characters following a sepcific pattern.
   * `[a-m]` 1st character: lowercase letter from `a` to `m`
   * `[c-z]` 2nd character: lowercase letter from `c` to `z`
   * `[4-9]` 3rd character: digit feom `4` to `9`
 
* `ls ???` files with exactly 3 characters
* `ls [A-Z]*[0-9]` files starting with uppper case, any middle, ending with digit.
* `ls [!.]*`  files not starting with dot (hidden files)
* `ls *.[tp][xd][tf]`   files with `.txt` or `.pdf` extensions
* `ls *~`  backup files (ending with ~)
* `ls *[0-9]` files with single digit in name
   
      nsivareddy@X-J3PVH32KM4 dummy % touch ac4 bz9 mz4 ad3 nz4 ac5 az9 bd8 zz9 
      nsivareddy@X-J3PVH32KM4 dummy % ls [a-m][c-z][4-9]
      ac4	ac5	az9	bd8	bz9	mz4

* Complete Comparison Table: 

<img width="735" height="282" alt="image" src="https://github.com/user-attachments/assets/bfc8ed18-2eb9-47a9-a948-f62aa46946d6" />

* History commands:
  
       !!    repeat last command
       !ls   repeat last command starting with ls
       !5    repeat command #5 from history
       !$    last argumnet of previous commmand
       !*    all the arguments of prevous command
* Examples of history commands:

      # List multiple files
      ls file1.txt file2.txt file3.txt
      
      # Copy all those files to a directory
      cp !* /backup/
      # Expands to: cp file1.txt file2.txt file3.txt /backup/
      
      
      # Change permissions on multiple files
      chmod 644 report.pdf invoice.pdf contract.pdf
      
      # Now change owner of the same files
      chown user:group !*
      # Expands to: chown user:group report.pdf invoice.pdf contract.pdf
      
      # Check files
      ls *.log *.tmp *.cache
      
      # Move all of them
      mv !* /tmp/
      # Expands to: mv *.log *.tmp *.cache /tmp/
      
      
      # Download files
      wget file1.zip file2.zip file3.zip
      
      # Unzip all of them
      unzip !*
      # Expands to: unzip file1.zip file2.zip file3.zip
      # (Though this would only unzip file1.zip; you'd need a loop for all)
      
      # View configuration files
      cat nginx.conf php.ini mysql.cnf
      
      # Backup all of them
      cp !* /backup/configs/
      # Expands to: cp nginx.conf php.ini mysql.cnf /backup/configs/

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

* **Side-by-side comparison**:
  
      # Command with multiple arguments
      touch file1.txt file2.txt file3.txt
      
      # Use !$ (last argument only)
      ls !$
      # Expands to: ls file3.txt
      
      # Use !* (all arguments)
      ls !*
      # Expands to: ls file1.txt file2.txt file3.txt
* **Working with git**:
  
      # Clone a repository
      git clone https://github.com/user/myproject.git
      
      # Navigate into it
      cd !$
      # Expands to: cd myproject.git
      # (Note: you'd actually want the directory name, which is 'myproject')
      
      # Better approach:
      git clone https://github.com/user/myproject.git myproject
  
* **File Management**:
   
      # Create multiple directories
      mkdir docs images videos scripts
      
      # Set permissions on all of them
      chmod 755 !*
      # Expands to: chmod 755 docs images videos scripts
* **Text Processing**:
  
      # Concatenate files
      cat header.txt body.txt footer.txt
      
      # Combine them into one
      cat !* > complete.txt
      # Expands to: cat header.txt body.txt footer.txt > complete.txt
* **System Administration**:
  
      # Stop services
      systemctl stop nginx mysql redis
      
      # Check status of the same services
      systemctl status !*
      # Expands to: systemctl status nginx mysql redis
* **Find and Act**:
  
      # Find large files
      find /var/log -name "*.log" -size +100M
      
      # Delete them (be careful!)
      rm !$
      # Expands to: rm -size (WRONG! This is the last argument, not what you want)
      
      # For this case, you'd want to use:
      rm $(find /var/log -name "*.log" -size +100M)
  
<img width="625" height="328" alt="image" src="https://github.com/user-attachments/assets/ced7c2b2-a053-47aa-9c36-fd37ea54c397" />

* **Practical Interactive Examples**:
* **1. File Operations**:
      $ echo "Hello World" > message.txt
      $ cat !$
      cat message.txt
      Hello World
      
      $ ls -l message.txt
      -rw-r--r-- 1 user group 12 Nov 26 10:30 message.txt
      
      $ chmod 600 !$
      chmod 600 message.txt
      
      $ ls -l !$
      ls -l message.txt
      -rw------- 1 user group 12 Nov 26 10:30 message.txt

* **Multiple Files**:
  
      $ touch file1 file2 file3
      $ ls !*
      ls file1 file2 file3
      file1  file2  file3
      
      $ chmod 644 !*
      chmod 644 file1 file2 file3
      
      $ ls -l !*
      ls -l file1 file2 file3
      -rw-r--r-- 1 user group 0 Nov 26 10:30 file1
      -rw-r--r-- 1 user group 0 Nov 26 10:30 file2
      -rw-r--r-- 1 user group 0 Nov 26 10:30 file3
* **Directiry Operations**:
  
      $ mkdir -p projects/website/src
      $ cd !$
      cd projects/website/src
      
      $ pwd
      /home/user/projects/website/src
      
      $ touch index.html style.css script.js
      $ ls !*
      ls index.html style.css script.js
      index.html  script.js  style.css
* **Combing with Other Commands**:
  
      # Create file and immediately edit
      touch newfile.txt && vim !$
      # Expands to: touch newfile.txt && vim newfile.txt
      
      # Download and verify
      wget https://example.com/package.tar.gz && md5sum !$
      # Expands to: wget https://example.com/package.tar.gz && md5sum package.tar.gz
      
      # Compile and run
      gcc program.c -o program && ./!$
      # Expands to: gcc program.c -o program && ./program

* **Using Pipes**:
  
      # Find files and act on last one
      find . -name "*.txt"
      # ... shows list of files ...
      
      # Edit the last one found? No, !$ would be the find command's last arg
      # Better to use: vim $(find . -name "*.txt" | tail -1)
* **!^ - First Argument**:
  
      $ cp /etc/hosts /tmp/hosts.backup
      $ cat !^
      cat /etc/hosts
* **!:2 - Specific Argument(2nd in this case)**:
  
      $ cp source.txt destination.txt /backup/
      $ ls !:2
      ls destination.txt
* **!:2-$ - Range of Argumants (2nd to last)**:
  
      $ echo one two three four five
      $ echo !:2-$
      echo two three four five
      two three four five
* **Entire Previous Command**:
* 
      $ cat /etc/shadow
      Permission denied
      
      $ sudo !!
      sudo cat /etc/shadow
      # Now it works!
* **View before Executing**:
* **See what will Expand(:p modifier)**:
  
      $ ls file1 file2 file3
      $ echo !*:p
      # Shows: echo file1 file2 file3
      # Doesn't execute, just prints
      
      $ echo !*
      # Now executes: echo file1 file2 file3
  

* **Common Pitfalls and Solutions**:
* **1! with no Arguments**:
* 
      $ ls
      # If previous command had no arguments, !$ expands to nothing
      
      $ cd !$
      # Error or unexpected behavior
* **!* Including Unwanted Argumnets**:
  
          $ rm -rf /tmp/cache
          $ ls !*
          ls -rf /tmp/cache
          # Oops! Includes the -rf flag too!
          
          # Solution: Use specific argument numbers
          $ ls !$
          ls /tmp/cache
* **History Expansion in Scripts**: 

        # In scripts, history expansion is usually disabled
        # Use variables instead:
        last_arg=$_  # Special variable for last
  
* **Practical Cheat Sheet**:
      # Download and extract in one go
      wget URL && tar -xzf !$ && cd !$
      
      # Create directory and navigate
      mkdir mydir && cd !$
      
      # Copy files and verify
      cp file1 file2 destination/ && ls !$
      
      # Change permissions then owner
      chmod 755 script.sh && chown user:group !$
      
      # Git: Add and commit
      git add file1.txt file2.txt && git commit -m "Added !*"
* **Enabling/ Disabling History Expansion**:
* **Check if Enabled**:
  
      # In bash
      set -o | grep histexpand
      
      # In zsh
      setopt | grep hist
* **Disable Temporarily**:
  
      # Bash
      set +H
      
      # Zsh
      setopt no_bang_hist
* **Enable**:

      # Bash
      set -H
      
      # Zsh
      setopt bang_hist


<img width="616" height="212" alt="image" src="https://github.com/user-attachments/assets/bac4e23a-dbc3-4dc5-92a6-0055476afae5" />

* **Practice Exercise**:
  
      # 1. Create files
      touch apple.txt banana.txt cherry.txt
      
      # 2. List the last one
      ls !$
      # Should show: cherry.txt
      
      # 3. List all of them
      ls !*
      # Should show: apple.txt banana.txt cherry.txt
      
      # 4. Move all to a directory
      mkdir fruits
      mv !* fruits/
      # Should move: apple.txt banana.txt cherry.txt to fruits/
      
      # 5. Go to that directory
      cd !$
      # Should go to: fruits/

<img width="624" height="208" alt="image" src="https://github.com/user-attachments/assets/d19eba8f-6e31-4dc3-802e-a6d75bc40fe2" />

#### Remove file content without login to vi or vim:
* **Method 1: Using > (Redirect - Simplest)**:
  
      # Clear single file
      > connection_failed_servers.txt
      
      # Clear multiple files at once
      > connection_failed_servers.txt
      > chef_not_found_servers.txt
      > chef_version_report.txt
* **Method 2: Using truncate Command**:
  
      # Clear single file
      truncate -s 0 connection_failed_servers.txt
      
      # Clear multiple files
      truncate -s 0 connection_failed_servers.txt chef_not_found_servers.txt chef_version_report.txt
* **Method 3: Using echo with -n Flag**:
  
      echo -n > connection_failed_servers.txt
* **Method 4: Clear All Chef Output Files at Once**:
  
      # Clear all three output files
      > connection_failed_servers.txt && > chef_not_found_servers.txt && > chef_version_report.txt
      
      # Or using a loop
      for file in connection_failed_servers.txt chef_not_found_servers.txt chef_version_report.txt; do
          > "$file"
      done
* **Method 5: Using cat /dev/null**:

      cat /dev/null > connection_failed_servers.txt
* **Recommended Approach for Your Script 🎯**:
      
      Add this at the beginning of your chef_version.sh:
      #!/bin/bash
      
      # Clear previous results before starting
      > connection_failed_servers.txt
      > chef_not_found_servers.txt
      > chef_version_report.txt
      
      # Rest of your script...
      for node in $(cat server-list.txt); do
          ...
      #!/bin/bash# Clear previous results before starting> connection_failed_servers.txt> chef_not_found_servers.txt> chef_version_report.txt# Rest of your script...for node in $(cat server-list.txt); do    ...
* **Or Create a Cleanup Script**:
  
      # Create cleanup.sh
      cat > cleanup.sh << 'EOF'
      #!/bin/bash
      echo "Clearing output files..."
      > connection_failed_servers.txt
      > chef_not_found_servers.txt
      > chef_version_report.txt
      echo "Done! Files cleared."
      EOF

      chmod +x cleanup.sh
* **Quick One-Liner for All Files**:
      
      # Clear all .txt files in current directory (be careful!)
      for f in *.txt; do > "$f"; done
      
      # Or specifically just the output files
      for f in connection_failed_servers.txt chef_not_found_servers.txt chef_version_report.txt; do > "$f"; done
      # Run it before executing chef_version.sh
      ./cleanup.sh
      ./chef_version.sh

 <img width="616" height="216" alt="image" src="https://github.com/user-attachments/assets/c500bf71-529c-4276-a8c2-062e9b45503c" />

#### Symbolic links:
* There are two types of links available.
 * `Soft link`:
   * Size of link file is equal to the no. of characters in the name of original file.
   * Can be created across the Partition.
   * Inode (index) no. of source and link file is different.
   * If original file is deleted, link is broken and data is lost.
   * Shortcut file.
* `Hard link`:
   * Size of both files isa same.
   * Can't be created across the partition.
   * Inode no. of both file is same.
   * If original file is deleted then also link will contain data.
   * Backup file.
* An inode (index node) is a data structure in Unix/Linux filesystems that stores metadata about a file or directory. Each file or directory has a unique inode number that serves as its identifier in the filesystem.
  
* **Creating a soft link**:
  * `ln -s <source file> <destination>`
   
        nsivareddy@X-J3PVH32KM4 ~ % cd  /Users/nsivareddy/practice/dir1 
        nsivareddy@X-J3PVH32KM4 dir1 % vi test
        there 
        are 
        some 
        lines 
        to test 
        soft link 
        
        nsivareddy@X-J3PVH32KM4 dir1 % ls -l
        total 8
        -rw-r--r--  1 nsivareddy  staff  47  2 Dec 19:14 test
        *  here 47 is size of the file
        
        
        nsivareddy@X-J3PVH32KM4 ~ % ln -s /Users/nsivareddy/practice/dir1/test .
        nsivareddy@X-J3PVH32KM4 ~ % ls -l test
        lrwxr-xr-x  1 nsivareddy  staff  36  2 Dec 19:16 test -> /Users/nsivareddy/practice/dir1/test
        
        * Here l is link file, size of link file is equal to the no of characters in the name of original file.
  * `nsivareddy@X-J3PVH32KM4 ~ % ln -s /Users/nsivareddy/practice/dir1/test test1` we don't need to specify the destination if we are in the same locationa and give any custom name or same name as oiginal file.
  * `ln -s /Users/nsivareddy/practice/dir1/test /Users/nsivareddy/practice/softlink` here we are the current woking directory is different than source and destination however created a socftlink shortcut with `softlink` file under '/Users/nsivareddy/practice/' path.
  * Softlink does not hold any data it is shortcut link to open for original file.
  * When we delete the link we will only loose the access but the original file will be available but when we delete the original file the link exists but file can't be accessed.

   <img width="556" height="204" alt="image" src="https://github.com/user-attachments/assets/15e3c3b9-b9ba-4062-aa7c-65c56d94a571" />
* To delete link file use  `rm -rf <softlink name>`.
* **Creating a soft link**:
* `ln <source file> <destination>`
* Incase if we don't want to loose the data once we delete a file or content hardlink backup will helps.
* If we exit the original file the data is copied to backup file and if we make any changes to original file the same changes will be applicable in original file with the help of inode since both have same inode number.
* If we update any of the original or hard link file both files will be auto updated.
* We can find the number of hardlink after the file permissions but it will not show which is the hardlink file path.
* Size of the both files is same with the same i node number.

        nsivareddy@X-J3PVH32KM4 practice % ln file1.txt /Users/nsivareddy/practice/dir1/hard
        
        nsivareddy@X-J3PVH32KM4 practice % ls -la file1.txt 
        -rw-r--r--  2 nsivareddy  staff  42  3 Dec 05:08 file1.txt
        
        nsivareddy@X-J3PVH32KM4 practice % ls -la /Users/nsivareddy/practice/dir1/hard
        -rw-r--r--  2 nsivareddy  staff  42  3 Dec 05:08 /Users/nsivareddy/practice/dir1/hard
* Both have same inode number.
  
        nsivareddy@X-J3PVH32KM4 practice % ls -i /Users/nsivareddy/practice/dir1/hard
        51304437 /Users/nsivareddy/practice/dir1/hard
        nsivareddy@X-J3PVH32KM4 practice % ls -i file1.txt
        51304437 file1.txt
* If we delete the original file the original file will be unaffected, the only change we can find is the number of links will be updated to 1 from1.
* We can't find the hardlink files. The only one method to find hardlink is with `inode number`.
* We can search the file with the same inode number to find hardlink files. `find / -inum <inode number>`

<img width="244" height="32" alt="image" src="https://github.com/user-attachments/assets/94207807-5b9d-43ee-997f-c270901d45a3" />
   

    <img width="565" height="201" alt="image" src="https://github.com/user-attachments/assets/bad18db5-23a4-4253-b91f-355b8f6c11d3" />

    <img width="705" height="240" alt="image" src="https://github.com/user-attachments/assets/1036f4f6-157b-479c-9b07-50d4ddf13a49" />

#### Types of files:
 * `-` regular file
 * `d` directory
 * `b` blk device
 * `c` char
 * `l` linked file
 * `s` socketfile
 * `id`
 * `pid` process id (what are commands/programs that are running identified by pid)
 * `repoid` package management id is repo id
 * `index number/inode number` (ls -il <filename> --> to check inode number) each file which we create in system has index number.
 * each file has an unique inode number it is defined as table of indexes for all the uniqueness associated for each file. Which gives the information of the file except file name
###### Hardlink file:
* It is a backup file
* Only applied to the files
* If original file is deleted there is a backup
* Inode number is same
* Difficult to identify
* It is stored only within the file system
* Hard link can only be used if both files are on the same file system. The file system heirarchy can be madeup of multiple storage devices. Depending on the configuration of your system, when you change intp a new directory, that directory and its contents may be stored on a different file system. 
###### Softlink file:
* Softlink is a shortcut file
* Can applied for files and directories
* If original file is deleted there is no use of softlink file
* Inode is different from the original file
* Easy to identify
* It can store any file system (nfs, mount, windows file system)

  <img width="556" height="440" alt="image" src="https://github.com/user-attachments/assets/49ba3fca-4d17-44ef-a08c-8da39d152912" />

* `copy` and `hardlink` both are different sice copy is used to copy the file from one location to another but in case of hardlink the same file get updated in the both places.

  <img width="440" height="355" alt="image" src="https://github.com/user-attachments/assets/7c22b91c-33bb-4603-a7ca-20aac726e4bb" />

  <img width="477" height="351" alt="image" src="https://github.com/user-attachments/assets/72067a3c-4d35-4163-9ab9-d03253ddebbf" />

#### User Group Management:
* Every one who login to computer is a user. User is used to authorize a person or to access system resources we add a user and user name is unique due to UID. 
* Every file or folder in linux system is owned by a particular user.
* Every process or running program run by a particular user.
* `User` is an entity that can access the system and its resources. Every user has:
  * A unique username(login name).
  * A unique UID(User ID) - a numberic number
  * A home directory (usually /home/username)
  * A default shell (e.g., /bin/bash)
* `Group` is a collection of users. Groups simplify permission management by allowing you to grant access to multiple users at once. Each group has:
  * A unique group name
  * A unique GID (Goup ID)
  * A list of member users
* `Users and Group purpose`:
   * Security --> Isolate processes and data; users can only access what they have permitted.
   * Access Control --> Define who can read, write or execute files and directories
   * Accountability --> Track who did what on the system (auditing/logging)
   * Resource Management --> Limit CPU, memory, disk usage per user
   * Multi-user Support --> Allow multiple people to use the same sytem safe
* `User typs in Unix`:
  * 1. Root User (Super user):
    * UID: 0
    * Home directory is `/root` and all commands are stores in `/var/sbin`, default shell access to super user is `/bin/bash`
    * Has unlimited access to the entire system
    * Can modify any file, kill any perocess, change any setting
    * Username is typically root
  * 2.System User(Service Account)/ Network user:
    * UID range: typically 1-99 (Varies by distribution)
    * Created automatically for running services/daemons
    * Examples: www-data, mysql, nginx, nobody, ftp, ldap, nfs, sambauser, apache
    * Usually have no login shell (/usr/sbin/nologin or /bin/false)
    * can't log in interactively
  * 3. Normal/ Regular Users(Normal Users):
    * UID range: typically 1000+ upto 60000, home directiory is `/home` and default shekll is `/bin/bash`
    * The user added by super user.
    * Limited permissions (can not typically system files)
  * 4. Sudo User:
    * Sudouser is a normal user with root previlege. 
    * In case admin is absent and the user want to install some packages/ want to create a d directory.
  * To check the default login details for the user we can find under `vim /etc/login.defs`
  * System account user id range is from 201 to 999
* Key files
   
      file           purpopse
      /etc/passwd    User account information
      /etc/shadow    Encrypted passwords (Restricted access only for root)
      /etc/group     Group definitions
      /etc/gshadow   Group passwords(raralely used)
      gettent passwd List all users including LDAP/network users
* Detailed user Info:
  
      # Full details for specific user
      getnent passwd reddy
      # Finger (if installed)
      finger reddy
      
      # Check user exists
      id reddy
      
      # User's group
      groups reddy

* List Admin/Sudo Users:
  
      # Users in sudo group (Debian/Ubuntu)
      getent group sudo
      
      # Users in wheel group (CentOS/RHEL/Fedora)
      getent group wheel
      
      # Check sudoer file
      sudo cat /etc/sudoers


* `id username 2>/dev/null && echo "exists" || echo "not exists"` check if user name exists or not.
* `last` last logins
* `who`  currently loggedin
* `sudo lastb` failed login attemps (security)
* Example: `/etc/passwd` Entry
  
      username:password:UID:GID:comment:home:shell    
      username:x:1001:1001:Full Name:/home/username:/bin/bash
         │     │   │    │      │           │            │
         │     │   │    │      │           │            └── Default shell
         │     │   │    │      │           └── Home directory
         │     │   │    │      └── Comment (usually full name)
         │     │   │    └── Primary GID
         │     │   └── UID
         │     └── Password placeholder (actual password in /etc/shadow)
         └── Username
  
* Modify the default: username:password:UID:GID:comment:home:shell
  
        cat /etc/shells                                   list all shells.
        usermod -s /bin/sh <user_name>                    change default shellfor that particular user.
        useradd -D                                        Give default home directory of the user info
        usermod -d /<group_name>/<user_name> <user_name>  Change defult home directory
        usermod -c "comment/group name" <user_name>       Chnage comment/ group name
        usermod -u <custom_userID> <user_name>            Change deault user name
        usermod -g <groupID> <user_name>                  Change default group
        grep <user_name> /etc/shadow                      Check if the password is applied or not
        passwd stdin <user_name>                          update password to the user
        usermod -l <New_user_name> <old_user_name>        Changes user name
  
  * We need to change user id incase of ex. banking account to link all other service of the bank for a single user
  * If `username:!!...` the user is not assigned password.
  * This user name is required in case if we need to provide alias name in company mail id since every company will have their own website name. 
  

   <img width="496" height="440" alt="image" src="https://github.com/user-attachments/assets/3b815c44-ee46-4624-8f34-70a582402c45" />

   <img width="803" height="650" alt="image" src="https://github.com/user-attachments/assets/b0863cbc-6dd5-4512-adf1-d95dc5de87df" />
* **Question:** Add a user SivaReddy with uid 6000 gid 1000 comment dba homedir /visitors shell /bin/sh  passwd hkdgwhlkgw
* mkdir /visitors
* usermod -u 6000 -g 1000 -c "dba" -d /visitors -m -s /bin/bash sivareddy    ==> with m to copy home diredctory, default home directory changed to /visitors now
* usermod -u 8443 -g 1000 -c "sa" -d /visitors/siva -s /bin/bash siva          ==> Now all users will be created by default in vistors directory
* find / -user <user_name>              provides the user name path 
* `useradd ram` is created in `/var/spool/mail/ram` location If we want to create a user and change the directiry. Wew need to modify `vim /default/useradd` after addingusers to visitors to home directory present in `/var/spool.mail` Since we didn't copy hidden files we will get errroas `Not copying file from skel directory into it` with `cp .b* /Visitors`.
* No come out of the directory add user `useradd sam` and swicth sam user `sudo su - sam`pwd will give `/bvisitors/sam`.
* User is not created inside home directory user login and user profiles all in inside `/etc/skel` folder it is recommend not to change.
* We can chage in the default settings as nroot user , regualr user can't modify id it is sudo previlege users then after we need to copy all hidden files to that particular folder then whatever user we create it will not be created inside hoem directory and creates in custom directory.
     
  <img width="763" height="762" alt="image" src="https://github.com/user-attachments/assets/b51a16dc-4589-48df-861d-dd986dff0ea3" />
* Normal user don't need to change default setting by default it would be `home`  but if we want to mount a network user ex LADP(Lightweight Directory Access Protocol) which is a protocol for acccessing and managing directory services - Centralized databasse storibng user accounts, groups and other organizational data.
* LDAP user or samba users are not auto mounted inside home directory we have to create another directory.
* To change the home directory of user using usermod command, instead of this we can modify `/etc/passwd` directory all thse 7 fields there.
* Once the fiel got saved and switch the user
* When a new user is added the user info is stored under `/etc/passwd` once the user is deleted only `/etc/passwd` will be delete with `userdel <username>` comand but it will not delete all places ie `home`,`skel` folder, `all hidden files` and `/var/spool/mail`  will remains and does not allow to recreate the same user as the user details remains in the other folders.
* `userdel -r <user_name>` delete user name from all the locations.
  
  <img width="662" height="371" alt="image" src="https://github.com/user-attachments/assets/5ca63739-d508-4325-ac88-0902b5bbfadd" />

* Once we edit `/etc/passwd` the skel and hidden directories are copied in RHEL8 but in RHEL7 we need to copy manually with `cp` command.
  
  <img width="504" height="331" alt="image" src="https://github.com/user-attachments/assets/f153dd49-4c02-45ca-8c5c-1e1921f04164" />


* **/etc/passwd:**
* This file stores encrypted passwords and password-related information for user accounts. It is readable by root user only.
  
        # Check permissions
        ls -l /etc/shadow
        # -rw-r----- 1 root shadow 1234 Dec 4 10:00 /etc/shadow
* `File format:` Each line represnts one user with 9 fields separed by (:)
  
        username:password:lastchg:min:max:warn:inactive:expire:reserved
        reddy:$6$xyz123$ABCdef.../...:19876:0:99999:7:::

* `Field Breakdown`:
  
         #   Filed         Example                 Meaning
  
         1 Username        reddy                  Account name
         2 Password        $6$xyz123$hash         Encrypted password
         3 Last Change     19876                  Days Since Jan 1,1970 password was changed 
         4 Min days        0                      Min days before password can be changed
         5 Max days        99999                  Max days password is valid
         6 Warn days       7                      Days before expiry account in warn user
         7 Inactive                               Days after expiry account is disabled
         8 Expire                                 Date account expires (days since epoch)
         9 Reserved                               Reserved for future use
* `Password Field Values`:

        value                Meaning
  
        $6$xyz123$hash      SHA-512 encrypted password
        $5$xyz123$hash      SHA-216 encrypted password
        $1$xyz123$hash      MD5 encrypted (old, weak)
        *                   Account disabled, no password login
        !                   Account locked
        !!                  Password neverset
        !$6$...             Locked account(! prefix)
        (empty)             No password required (dangerous)
         
* `Password Hash Prefixes`:
  
        Prefix        Algorithm
        $1$           MD5
        $5$           SHA-256
        $6$           SHA-512 (recommended)
        $y$           yescrypted(newer)
* Real Exampple:
  
        sudo cat /etc/shadow
  
        root:$6$rounds=5000$saltsalt$longhashhere...:19800:0:99999:7:::  ==> root      --> has password
        daemon:*:19500:0:99999:7:::                                      ==> daemon    --> Disabled(*)
        nobody:*:19500:0:99999:7:::                                      ==> nobody    --> Diabled(*)
        reddy:$6$aBcDef$xyz123hashvalue...:19876:0:99999:7:::            ==> reddy     --> Has password
        john:!!:19850:0:99999:7:::                                       ==> john      --> Password never set(!!)
        locked_user:!$6$salt$hash...:19800:0:99999:7:::                  ==> Locked_user --> Locked(! Prefix)
* **Change /Update Password**:
  * `Using passwd(recommended)`:
    
        # Change your own password
        passwd
        
        # Change another user's password (as root)
        sudo passwd reddy
        
        # Force user to change password on next login
        sudo passwd -e reddy

  * `Using chpasswd(Batch/Scripts)`:
    
        # Single user
        echo "reddy:newpassword" | sudo chpasswd
        
        # Multiple users from file
        sudo chpasswd < passwords.txt
        
        # With encrypted password
        echo "reddy:$6$salt$hashedpassword" | sudo chpasswd -e
  * `Using usermod`:
    
        # Set encrypted password directly
        sudo usermod -p '$6$salt$hashedpassword' reddy


* **Lock/Unlock Account:**
  * Lock Account:
    
        # Method 1: passwd
        sudo passwd -l reddy
        
        # Method 2: usermod
        sudo usermod -L reddy
        
        # Verify (shows ! prefix)
        sudo grep reddy /etc/shadow
        # reddy:!$6$salt$hash...:19876:0:99999:7:::
  * Unlock Account:
   
        # Method 1: passwd
        sudo passwd -u reddy
        
        # Method 2: usermod
        sudo usermod -U reddy

* Password Aging/Expiry:
** View Password info
  
      # check password status
      sudo change -l reddy
      
  * Output: 
      Last password change                    : Dec 04, 2025
      Password expires                        : never
      Password inactive                       : never
      Account expires                         : never
      Minimum number of days between changes  : 0
      Maximum number of days between changes  : 99999
      Warning days before password expires    : 7
* Set Password Policies:
  
      # Force password change on next login
      sudo chage -d 0 reddy
      
      # Set password expiry to 90 days
      sudo chage -M 90 reddy
      
      # Set minimum days between changes
      sudo chage -m 7 reddy
      
      # Set warning days before expiry
      sudo chage -W 14 reddy
      
      # Set account expiration date
      sudo chage -E 2025-12-31 reddy
      
      # Interactive mode
      sudo chage reddy
* Don't have access:
 * Forget Root Password
   * Single user mode(GRUB):
     
          # 1. Reboot and hold SHIFT to get GRUB menu
          # 2. Press 'e' to edit boot entry
          # 3. Find line starting with 'linux' and add at end:
          init=/bin/bash
          
          # 4. Press Ctrl+X to boot
          # 5. Remount filesystem as writable
          mount -o remount,rw /
          
          # 6. Change password
          passwd root
          
          # 7. Reboot
          exec /sbin/init
   * Recovery Mode(Ubuntu):
     
          # 1. Boot into recovery mode from GRUB
          # 2. Select "root - Drop to root shell prompt"
          # 3. Remount filesystem
          mount -o remount,rw /
          
          # 4. Change password
          passwd root
          # or
          passwd username
          
          # 5. Reboot
          reboot

    * Live USB:
          # 1. Boot from Live USB
          # 2. Mount the system partition
          sudo mount /dev/sda1 /mnt
          
          # 3. Chroot into the system
          sudo chroot /mnt
          
          # 4. Change password
          passwd root
          
          # 5. Exit and reboot
          exit
          sudo reboot
 * User Account Locked:
   
          # Check if locked
          sudo passwd -S reddy
          # reddy L 12/04/2025 0 99999 7 -1 (Password locked.)
          
          # Unlock
          sudo passwd -u reddy
          
          # Or set new password (also unlocks)
          sudo passwd reddy
 * Password Never Set(!!):

          # Set initial password
          sudo passwd reddy
 * No Sudo Access:
   
          # If you have physical access, use recovery mode (above)
          
          # If another admin exists, ask them to:
          sudo passwd your_username
          
          # Or add you to sudo group
          sudo usermod -aG sudo your_username  # Debian/Ubuntu
          sudo usermod -aG wheel your_username  # CentOS/RHEL
 * Quick Reference:
   
          sudo cat /etc/shadow              view shadow file
          sudo passwd username              Change password
          sudo passwd -l username           Lock account
          sudo passwd -u username           Unlock account
          sudo passwd -S username           Check p[assword status
          sudo chage -l username            View expiry info
          sudo chage -d 0 username          Force password change
          sudo chage -M 90 username         Set max password age
          openssl passwd -6 "password"      Generate passowrd hash
          sudo vipw -s                      safe edit shadow 
 * Security best practices:
   
          # Ensure correct permissions
          sudo chmod 640 /etc/shadow
          sudo chown root:shadow /etc/shadow
          
          # Check for users with empty passwords (security risk!)
          sudo awk -F: '($2 == "") {print $1}' /etc/shadow
          
          # Check for users with no password aging
          sudo awk -F: '($5 > 99999) {print $1}' /etc/shadow


* Common commands:
  
        # user management
  
        whoami                 # Shows current username
        id                     # Shows UID, GID, and groups
        echo $USER             # Jsut user name
        useradd username       # Create a new user
        userdel username       # Delete a user
        passwd username        # Change password
        who or w               # Who is logged in right now
          
        # Grouop Management:
        groups                  # Shows groups for current user
        groupadd groupname      # Create a new group
        usermod -aG group user  #  Add user to a group

* Permission Model:
  * Linux uses users and groups in its permission system:
  
        -rwxr-xr-- 1 alice developers 4096 Dec 4 10:00 script.sh
         │││ │││ │││    │       │
         │││ │││ │││    │       └── Group owner
         │││ │││ │││    └── User owner
         │││ │││ └└└── Others (everyone else)
         │││ └└└── Group permissions
         └└└── User/Owner permissions

* Commands on user ids:

          # Check your own ID
          id
          
          # Check specific user
          id reddy
          
          # List all groups
          groups reddy
          
          # Check if user can sudo
          sudo -l -U reddy
          
          # List all users in admin group
          dscl . -read /Groups/admin GroupMembership
  
  
