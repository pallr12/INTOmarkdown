#Open Source

Hópmeðlimir:

* palleydal
* pallr12

## 1. Linux uppsetning

I downloaded an Ubuntu image and installed it on a USB stick. There were no complications during the installation, and everything was up and running in "no" time.

## 2. Uppsetning á vim && git

The installation of Vim and Git was straightforward. So, I will put the output from the terminal in here as a reference of how it went.

1) Installing Vim  
ubuntu@ubuntu:~$ sudo apt-get install vim  
Reading package lists... Done  
Building dependency tree  
  
Reading state information... Done  
The following extra packages will be installed:  
  vim-runtime  
Suggested packages:  
  ctags vim-doc vim-scripts  
The following NEW packages will be installed:  
  vim vim-runtime  
0 upgraded, 2 newly installed, 0 to remove and 0 not upgraded.  
Need to get 5,825 kB of archives.  
After this operation, 28.0 MB of additional disk space will be used.  
Do you want to continue [Y/n]? y  
Get:1 http://archive.ubuntu.com/ubuntu/ saucy/main vim-runtime all 2:7.4.000-1ubuntu2 [4,880 kB]  
Get:2 http://archive.ubuntu.com/ubuntu/ saucy/main vim amd64 2:7.4.000-1ubuntu2 [945 kB]  
Fetched 5,825 kB in 8s (649 kB/s)  
Selecting previously unselected package vim-runtime.  
(Reading database ... 168741 files and directories currently installed.)  
Unpacking vim-runtime (from .../vim-runtime_2%3a7.4.000-1ubuntu2_all.deb) ...  
Adding 'diversion of /usr/share/vim/vim74/doc/help.txt to /usr/share/vim/vim74/doc/help.txt.vim-tiny by vim-runtime'  
Adding 'diversion of /usr/share/vim/vim74/doc/tags to /usr/share/vim/vim74/doc/tags.vim-tiny by vim-runtime'  
Selecting previously unselected package vim.  
Unpacking vim (from .../vim_2%3a7.4.000-1ubuntu2_amd64.deb) ...  
Processing triggers for man-db ...  
Setting up vim-runtime (2:7.4.000-1ubuntu2) ...  
Processing /usr/share/vim/addons/doc  
Setting up vim (2:7.4.000-1ubuntu2) ...  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vim (vim) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vimdiff (vimdiff) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rvim (rvim) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rview (rview) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vi (vi) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/view (view) in auto mode  
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/ex (ex) in auto mode  
  
2) Installing Git  
ubuntu@ubuntu:~$ sudo apt-get install git-core  
Reading package lists... Done  
Building dependency tree  
Reading state information... Done  
The following extra packages will be installed:  
  git git-man liberror-perl  
Suggested packages:  
  git-daemon-run git-daemon-sysvinit git-doc git-el git-email git-gui gitk  
  gitweb git-arch git-bzr git-cvs git-svn  
The following NEW packages will be installed:  
  git git-core git-man liberror-perl  
0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.  
Need to get 8,730 kB of archives.  
After this operation, 19.8 MB of additional disk space will be used.  
Do you want to continue [Y/n]? y  
Get:1 http://archive.ubuntu.com/ubuntu/ saucy/main liberror-perl all 0.17-1 [23.8 kB]  
Get:2 http://archive.ubuntu.com/ubuntu/ saucy/main git-man all 1:1.8.3.2-1 [670 kB]  
Get:3 http://archive.ubuntu.com/ubuntu/ saucy/main git amd64 1:1.8.3.2-1 [8,035 kB]  
Get:4 http://archive.ubuntu.com/ubuntu/ saucy/main git-core all 1:1.8.3.2-1 [1,386 B]  
Fetched 8,730 kB in 12s (695 kB/s)  
Selecting previously unselected package liberror-perl.  
(Reading database ... 170364 files and directories currently installed.)  
Unpacking liberror-perl (from .../liberror-perl_0.17-1_all.deb) ...  
Selecting previously unselected package git-man.  
Unpacking git-man (from .../git-man_1%3a1.8.3.2-1_all.deb) ...  
Selecting previously unselected package git.  
Unpacking git (from .../git_1%3a1.8.3.2-1_amd64.deb) ...  
Selecting previously unselected package git-core.  
Unpacking git-core (from .../git-core_1%3a1.8.3.2-1_all.deb) ...  
Processing triggers for man-db ...  
Setting up liberror-perl (0.17-1) ...  
Setting up git-man (1:1.8.3.2-1) ...  
Setting up git (1:1.8.3.2-1) ...  
Setting up git-core (1:1.8.3.2-1) ...  

## 3. Unnið með Git (1. hluti)

1) Installation of SSH keys  
ubuntu@ubuntu:~$ cd ~/.ssh
bash: cd: /home/ubuntu/.ssh: No such file or directory
ubuntu@ubuntu:~$ mkdir ~/.ssh
ubuntu@ubuntu:~$ ssh-keygen -t rsa -C "pallr12@ru.is"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/ubuntu/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/ubuntu/.ssh/id_rsa.
Your public key has been saved in /home/ubuntu/.ssh/id_rsa.pub.
The key fingerprint is:
5d:00:5f:a4:60:89:e7:a8:95:ac:84:1d:c8:ed:3c:8a pallr12@ru.is
The key's randomart image is:
+--[ RSA 2048]----+
| . o   .+o..o    |
|  o o ..oo +     |
|   = o =  o .    |
|  . * = .. .     |
| . o =  S .      |
|E . o            |
|                 |
|                 |
|                 |
+-----------------+
ubuntu@ubuntu:~$ ssh-add id_rsa
id_rsa: No such file or directory

2) Installation of Xclip
ubuntu@ubuntu:~$ sudo apt-get install xclip
Reading package lists... Done
lBuilding dependency tree       
Reading state information... Done
The following NEW packages will be installed:
  xclip
0 upgraded, 1 newly installed, 0 to remove and 2 not upgraded.
Need to get 19.0 kB of archives.
After this operation, 72.7 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu/ saucy/universe xclip amd64 0.12+svn84-2 [19.0 kB]
Fetched 19.0 kB in 0s (35.9 kB/s)
debconf: DbDriver "config": /var/cache/debconf/config.dat is locked by another process: Resource temporarily unavailable
Selecting previously unselected package xclip.
(Reading database ... 171132 files and directories currently installed.)
Unpacking xclip (from .../xclip_0.12+svn84-2_amd64.deb) ...
Processing triggers for man-db ...
debconf: DbDriver "config": /var/cache/debconf/config.dat is locked by another process: Resource temporarily unavailable
dpkg: error processing man-db (--unpack):
 subprocess installed post-installation script returned error exit status 1
No apport report written because MaxReports is reached already
                                                              Errors were encountered while processing:
 man-db
E: Sub-process /usr/bin/dpkg returned an error code (1)
ubuntu@ubuntu:~$ xclip -sel clip < ~/.ssh/id_rsa.pub
ubuntu@ubuntu:~$ ssh-keygen -t rsa -C "palleydal@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/ubuntu/.ssh/id_rsa): /home/ubuntu/.ssh/id_palleydal_rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/ubuntu/.ssh/id_palleydal_rsa.
Your identification has been saved in /home/ubuntu/.ssh/id_palleydal_rsa.pub.
The key fingerprint is:
80:3c:ad:46:68:ea:2d:21:11:67:0c:f1:4d:2f:d6:dc palleydal@gmail.com
The key's randomart image is:
+--[ RSA 2048]----+
|++o .            |
| =.= * .         |
|. + O * E        |
| + o + .         |
|o.  o   S        |
|o o.             |
| o .             |
|  .              |
|                 |
+-----------------+
ubuntu@ubuntu:~$ xclip -sel clip < ~/.ssh/id_palleydal_rsa.pub

3) Git clone for pallr12@ru.is
ubuntu@ubuntu:~$ git clone https://github.com/pallr12/INTOPrufa
Cloning into 'INTOPrufa'...
remote: Counting objects: 27, done.
remote: Compressing objects: 100% (19/19), done.
remote: Total 27 (delta 8), reused 19 (delta 1)
Unpacking objects: 100% (27/27), done.
Checking connectivity... done
ubuntu@ubuntu:~$ cd INTOPrufa
ubuntu@ubuntu:~/INTOPrufa$ vim NIM.cpp
ubuntu@ubuntu:~/INTOPrufa$ git commit -a -m "pallr12@ru.is commiting to git"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'ubuntu@ubuntu.(none)')
ubuntu@ubuntu:~/INTOPrufa$ git config user.email "pallr12@ru.is"
ubuntu@ubuntu:~/INTOPrufa$ git commit -a -m "pallr12@ru.is committing to git"
[master 3568899] pallr12@ru.is committing to git
 1 file changed, 1 insertion(+), 1 deletion(-)
ubuntu@ubuntu:~/INTOPrufa$ git push origin master
Username for 'https://github.com': pallr12
Password for 'https://pallr12@github.com': 
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To https://github.com/pallr12/INTOPrufa
   3430d1b..3568899  master -> master

4) Git clone for palleydal@gmail.com
ubuntu@ubuntu:~$ git clone https://github.com/pallr12/INTOPrufa
Cloning into 'INTOPrufa'...
remote: Counting objects: 33, done.
remote: Compressing objects: 100% (24/24), done.
remote: Total 33 (delta 10), reused 25 (delta 2)
Unpacking objects: 100% (33/33), done.
Checking connectivity... done
ubuntu@ubuntu:~$ cd INTOPrufa
ubuntu@ubuntu:~/INTOPrufa$ vim NIM.cpp
ubuntu@ubuntu:~/INTOPrufa$ git config user.email "palleydal@gmail.com"
ubuntu@ubuntu:~/INTOPrufa$ git commit -a -m "palleydal@gmail.com committing to git"
[master c83c683] palleydal@gmail.com committing to git
 1 file changed, 1 insertion(+), 1 deletion(-)
ubuntu@ubuntu:~/INTOPrufa$ git push origin master
Username for 'https://github.com': palleydal
Password for 'https://palleydal@github.com': 
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To https://github.com/pallr12/INTOPrufa
   3568899..c83c683  master -> master

5) Description of the process
This took me a couple of tries, since I was trying to imitate a group of two people. However, when I realised the functionality of the system (strangely) this became a lot of fun. I will definitely use this more in the future, whether I will be working in a group or by myself. This is just too valuable and easy to use, for me to not do it.

6) Link to the project
[https://github.com/pallr12/INTOmarkdown](https://github.com/pallr12/INTOmarkdown)

## 4. Uppsettur hugbúnaður

Since I am using the same computer for "all" group members I will only hand in one list.


| Program         | Version | License | Source Repository                                                |
| --------------- | ------- | ------- | ---------------------------------------------------------------- |
| gedit           | 3.8.3   | GPLv2   | [gedit repository](http://git.gnome.org/browse/gedit)            |
| Mozilla Firefox | 24.0    | MPLv2   | [Firefox repository](https://hg.mozilla.org/mozilla-central)      |
| LibreOffice     | 4.1.2.3 | LGPLv3  | [LibreOffice repository](http://cgit.freedesktop.org/libreoffice) |

## 5. Unnið með Git (2. hluti)

Hér þarf ekkert að gera annað en að setja niðurstöður úr 4. fyrstu liðunum inn í þetta skjal.
