(base) hallgato@tanterem:~$ conda install -c anaconda git
Collecting package metadata (current_repodata.json): done
Solving environment: done

# All requested packages already installed.

(base) hallgato@tanterem:~$ git clone https://github.com/patakrik/Szoftverfejleszt-s
Cloning into 'Szoftverfejleszt-s'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
(base) hallgato@tanterem:~$ ls
anaconda3     eclipse.desktop    netbeans-11.2     Sablonok
Asztal        eclipse-workspace  NetBeansProjects  Szoftverfejleszt-s
bogomips      examples.desktop   Nyilvános         vegtelen
bogomips.c    IdeaProjects       pattogas.cpp      vegtelen.cpp
DEADJOE       Képek              prog1             Videók
Dokumentumok  Letöltések         Projects          Zenék
(base) hallgato@tanterem:~$ ls Szoftverfejleszt-s/
README.md
(base) hallgato@tanterem:~$ mkdir szoft
(base) hallgato@tanterem:~$ cd szoft/
(base) hallgato@tanterem:~/szoft$ git init
Initialized empty Git repository in /home/hallgato/szoft/.git/
(base) hallgato@tanterem:~/szoft$ ls -la
összesen 12
drwxr-xr-x  3 hallgato hallgato 4096 febr  25 08:22 .
drwxr-xr-x 42 hallgato hallgato 4096 febr  25 08:21 ..
drwxr-xr-x  6 hallgato hallgato 4096 febr  25 08:22 .git
(base) hallgato@tanterem:~/szoft$ git config --global user.name "Patrik"
(base) hallgato@tanterem:~/szoft$ git config --global user.email "patak1998@gmail.com"
(base) hallgato@tanterem:~/szoft$ git remote add origin https://github.com/patakrik/Szoftverfejleszt-s
(base) hallgato@tanterem:~/szoft$ git pull origin master
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/patakrik/Szoftverfejleszt-s
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
(base) hallgato@tanterem:~/szoft$ ls
README.md
(base) hallgato@tanterem:~/szoft$ touch 1.txt
(base) hallgato@tanterem:~/szoft$ ls
1.txt  README.md
(base) hallgato@tanterem:~/szoft$ git add *
(base) hallgato@tanterem:~/szoft$ git commit -m "Added 1.txt"
[master 649d77c] Added 1.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 1.txt
(base) hallgato@tanterem:~/szoft$ git push origin master
Username for 'https://github.com': patakrik
Password for 'https://patakrik@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 270 bytes | 270.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/patakrik/Szoftverfejleszt-s
   c82af44..649d77c  master -> master
(base) hallgato@tanterem:~/szoft$ git config credential.helper cache 3600
(base) hallgato@tanterem:~/szoft$ git status
On branch master
nothing to commit, working tree clean
(base) hallgato@tanterem:~/szoft$ git log
commit 649d77c4dd638f66ab0e131331ef028ada1fe64d (HEAD -> master, origin/master)
Author: Patrik <patak1998@gmail.com>
Date:   Tue Feb 25 08:30:27 2020 +0100

    Added 1.txt

commit c82af44e3d311cefe4ca12309ce9dae8005e5390
Author: Patrik <36334711+patakrik@users.noreply.github.com>
Date:   Tue Feb 25 08:19:55 2020 +0100

    Initial commit
(base) hallgato@tanterem:~/szoft$ git log --online
fatal: unrecognized argument: --online
(base) hallgato@tanterem:~/szoft$ git log --oneline
649d77c (HEAD -> master, origin/master) Added 1.txt
c82af44 Initial commit
(base) hallgato@tanterem:~/szoft$ echo "Baromsag"> 1.txt
(base) hallgato@tanterem:~/szoft$ cat 1.txt 
Baromsag
(base) hallgato@tanterem:~/szoft$ git add *
(base) hallgato@tanterem:~/szoft$ git commit -m "nagyon jo commit"
[master 01eaadd] nagyon jo commit
 1 file changed, 1 insertion(+)
(base) hallgato@tanterem:~/szoft$ git log --oneline
01eaadd (HEAD -> master) nagyon jo commit
649d77c (origin/master) Added 1.txt
c82af44 Initial commit
