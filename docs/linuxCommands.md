# Some useful Linux Commands

Did you know that there are literally hundreds of Linux commands? Even on a bare-bones Linux server install there are easily over 1,000 different commands. The interesting thing is that most people only need to use a very small subset of those commands. I have listed down some commands that are used often with Logicboard 1. I'll add more commands as I find them to be used very often. 

## <span style="color:green">System Information</span>

### System info
    $ uname -a

### Kernel release info
    $ uname -r

### System host name
    $ hostname -I

### Who you are logged in as
    $ whoami


## <span style="color:green">Hardware Information</span>

### kernel messages
    $ dmesg

### CPU information
    $ cat /proc/cpuinfo

### Memory information
    $ cat /proc/meminfo

### USB devices info
    $ lsusb

### Connected hardware info
    $ lsblk


## <span style="color:green">File and Directory Commands</span>

### List files 
    $ ls -al

### Present working directory
    $ pwd

### New directory
    $ mkdir

### Go to previous directory
    $ cd ..

### Home directory
    $ cd

### Remove (delete) a file 
    $ rm file_name

### Remove directory
    $ rm -r directory_name

### Copy file 
    $ cp <source_file_location> <destination_file_location>

### Copy directory 
    $ cp -r <source_dir_location> <destination_dir_location>

### Rename or Move file 
    $ mv file1 file2

### Create an empty file
    $ touch file_name

### View contents of a file 
    $ cat file_name


##  <span style="color:green">File Permissions</span>

```
PERMISSION TYPE        COMMAND

   U   G   W
  rwx rwx rwx     chmod 777 filename
  rwx rwx r-x     chmod 775 filename
  rwx r-x r-x     chmod 755 filename
  rw- rw- r--     chmod 664 filename
  rw- r-- r--     chmod 644 filename

```
```
LEGEND
        U = User
        G = Group
        W = World

        r = Read
        w = write
        x = execute
        - = no access

```
## <span style="color:green">Networking</span>

### Network interfaces and IP address
    $ ip a

### eth0 address and details
    $ ip addr show dev eth0

### Internet connection test 
    $ ping www.google.com

### Network address of the host
    $ hostname -i

### Local IP addresses of host
    $ hostname -I

### Download
    $ wget http://domain.com/file


## <span style="color:green">Archives (TAR FILES)</span>

- Create tar named archive.tar for the directory directory_name: <br>
`$ tar cf archive.tar directory_name`
- Extract the contents from archive.tar: <br>
`$ tar xf archive.tar`
- Create a gzip compressed tar file name archive.tar.gz: <br>
`$ tar czf archive.tar.gz directory_name`
- Extract a gzip compressed tar file: <br>
`$ tar xzf archive.tar.gz`
- Create a tar file with bzip2 compression: <br>
`$ tar cjf archive.tar.bz2 directory_name`
- Extract a bzip2 compressed tar file: <br>
`$ tar xjf archive.tar.bz2`
- Extract xz file:<br>
`$ tar -xf directory_name.tar.xz`


## <span style="color:green">Installing Packages</span>

### Install package.rpm
    $ rpm -i package.rpm

### Install software from source code
    $ tar zxvf sourcecode.tar.gz
    $ cd sourcecode
    $ ./configure
    $ make
    $ make install



## <span style="color:green">SSH Logins</span>

### Connect to host as user
    $ ssh user@host

### Connect to host using port
    $ ssh -p port user@host


## <span style="color:green">File Transfers</span>

### Secure copy
    $ scp file.txt user@<server_ip_addr>:/usr/local

### Copy files from server to local machine
    $ scp user@<server_ip_addr>:/usr/local/*.txt /tmp

### Copy directories from server
    $ scp -r user@<server_ip_addr>:/usr/local/*.txt /tmp

### Synchronize
    $ rsync -a /home /backups/

### Sync files/directories between local and remote system
    $ rsync -avz /home user@<server_ip_addr>:/backups/
