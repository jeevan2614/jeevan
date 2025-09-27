# jeevan
activity 1
USING MAN COMMAND 
1)
ls -b → Shows non-printable characters as octal escapes.

ls -c → Sorts files by ctime (last status change) and shows ctime.

ls -d → Displays directories themselves, not their contents.

ls -e → Shows access time in full format.

ls -f → Disables sorting; lists entries in directory order.

ls -z → Prints security context (SELinux)

2) EXPLORE THE COMMAND
whoami       -- prints current logged-in username  
pwd          --prints current working directory  
cd           --change directory  
cd /         --go to root directory  
cd ..        --move one directory up  
cd <path>    -- move to a specific path

B)

--> tree -l -L 1

Shows only the first level of the directory tree, following symlinks.

--> tree -l -L 2

Shows two levels deep.

--> tree -l -L 3

Shows three levels deep.

--> tree /var/log/apt -La 1

Shows the contents of /var/log/apt, with:

-L 1 --> only first-level items

-a --> including hidden files

3. Example: tree -d /proc/self

The /proc directory is a virtual filesystem that provides process and system information.

/proc/self is a symlink that points to the current process’s directory in /proc/<pid>.

Running tree -d /proc/self shows only directories (-d).


Sample output breakdown:

/proc/self
|-- attr
|-- cwd -> /proc
|-- fd
|   `-- 3 -> /proc/15589/fd
|-- fdinfo
|-- net
|   |-- dev_snmp6
|   |-- netfilter
|   |-- rpc
|   |   |-- auth.rpcsec.context
|   |   |-- auth.rpcsec.init
|   |   |-- auth.unix.gid
|   |   |-- auth.unix.ip
|   |   |-- nfs4.idtoname
|   |   |-- nfs4.nametoid
|   |   |-- nfsd.export
|   |   `-- nfsd.fh
|   `-- stat
|-- root -> /
`-- task
    `-- 15589
        |-- attr
        |-- cwd -> /proc
        |-- fd
        |   `-- 3 -> /proc/15589/task/15589/fd
        |-- fdinfo
        `-- root -> /

Explanation of key items:

cwd -> /proc → current working directory symlink.

fd/ → file descriptors opened by the process.

fdinfo/ → details about each file descriptor.

net/ → network-related process info.

root -> / → symbolic link to the process root.

task/15589/ → represents the process’s threads/tasks.
At the bottom:
27 directories
Means total 27 directories were found under /proc/self.




