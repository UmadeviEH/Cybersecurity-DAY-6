# Cybersecurity-DAY-6
Cybersecurity Training Report — Day 11

Topic: Linux OS
 
FHS (File System Hierarchy Standard) — what goes where

Linux organizes files by purpose. Key top-level directories to remember:

/bin, /boot, /etc, /home, /lib, /media, /mnt, /opt, /root, /run, /srv, /tmp, /usr, /var, /sbin.

Analogy: like rooms in a house — each directory has a specific role.

Navigate the filesystem

pwd → show current directory.

ls, ls -la, ls -lh → list files (hidden, long format, human sizes).

cd /path / cd .. / cd ~ / cd / → move around directories.

Create, view, edit, remove files & folders

mkdir <dir> → make directory.

touch file → create empty file.

nano file (or vim) → edit file.

cp src dst → copy. mv src dst → move/rename.

rm file, rmdir dir (empty), rm -r dir → remove (use sudo if required).

Permissions & ownership (essentials)

Permission types: Read r = 4, Write w = 2, Execute x = 1.

Permission groups: User (owner), Group, Others. Example mode: -rwxr-xr--.

chmod symbolic: chmod u+rwx filename or chmod +x file.

chmod numeric: chmod 755 file (7=rwx owner, 5=r-x group, 5=r-x others).

Use chown user:group file to change ownership.

User & group management

sudo adduser <username> → create user.

sudo userdel <username> → delete user.

sudo groupadd <groupname> → create group.

sudo groupdel <groupname> → delete group.

Manage membership with usermod -aG <group> <user>.

Practical safety & study tips

Always check man <command> or --help before using unfamiliar commands.

Use history to review past commands.

Test destructive commands in a VM or container — never run risky commands on production.

Common dangerous example to avoid: rm -rf / (DON'T run).

Quick cheat-sheet 
pwd — current dir

ls -la — list all, long format

cd /path — change dir

mkdir dir — make folder

touch file — new file

nano file — edit file

cp src dst — copy

mv src dst — move/rename

rm file / rm -r dir — remove

chmod 755 file — set permissions (numeric)

chmod u+rwx file — set permissions (symbolic)

chown user:group file — change owner

sudo adduser user — add user

sudo groupadd group — add group
