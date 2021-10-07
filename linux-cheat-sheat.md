# Linux Cheat Sheat

#### Create new user:

* **useradd -m** _username_
  * -m creates a home directory for the user
* **passwd username**
* **usermod -a -G sudo** _username_
  * to add user to group, e.g. sudo
* **chsh -s /bin/bash** _username_
  * specify shell for a user?

### Installing packets for Debian and Ubuntu based systems:

**apt-get install** _pkg_

### Useful cmds:

* **uname -a** - kernel info
* **ifconfig/ ip addr show** - network informationq
* **netstat/ lsof -i -** info about ports/routing
* **df** - \(disk free \)display disk space
* **systemctl -** info about running services
* **du** - disk usage
* **top/htop/ps -** display CPU usage/precesses
* **ls /mnt -** list mounted devices
* **mount -** show existing mounts
  * e.g **mount /dev/sda2 /mnt -** mount sda2 device to /mnt
* **less /etc/fstab -** boot device list

**4 command types:**

1.  **An executable command**
2. **A command built in into the shell**
3. **A shell function**
4. **An Alias**

* **type** command - display cmd type
* **which** cmd - display executable location
* **help** cmd

 **rm -r** - remove directory and its content

**info/man coreutils -** dispaly info \(manual\) about cmd

Installing something:

* **sudo apt install** program

### Redirection

* **cat -** 
* **sort -** 
* **uniq -** 
* **grep -** 
* **wc -** 
* **head -** 
* **tail -** 
* **tee -**

\*\*\*\*

* **ls -l /usr/bin &gt; ls-output.txt -** send output results to a file
* **ls -l /usr/bin &gt;&gt; ls-output.txt -** append redirection to the same file \(no owerwrite\)
* **ls -l /bin/usr 2&gt; ls-error.txt -** redirect error to a file
* **ls -l /bin/usr &&gt; ls-output.txt** redirect output and error to the same file
  * 0 - input
  * 1 - output
  * 2 - error
* **/dev/null** - location to discard putput etc.
  * **ls -l /bin/usr 2&gt; /dev/nullls**

**Pipelines** used to filter commands

* **ls -l /usr/bin \| less**
* **ls -l /bin /usr/bin \| sort \| less -**  output of two directories sorted in one list
* **ls /bin /usr/bin \| sort \| uniq \| less** - removes any dublicates
* **ls /bin /user/bin \|sort \| uniq -d \| less -**  show list of dublicates

**wc: - Print word, line, byte counts**

**grep: Print lines matching pattern**

* **grep** _pattern filename_
* **ls /bin /usr/bin \| sort \| uniq \| grep zip** _-_ programs that have zip in the name

**head/tail - print first/last 10 lines**

**tail -f -** usefull for watching the progress of log files





