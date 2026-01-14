/home contains user directories. Your personal space is /home/milovan.
~ is a shortcut that always points to your home directory.

Every file and directory in Linux has:
an owner (user)
a group
others (everyone else)

Permissions are always split into three sections: d/owner(---)/group(---)/others(---) it looks like drwd------

Each section can have three permissions:
read (r)
write (w)
execute (x)

Numeric permission values:
r = 4
w = 2
x = 1

The sum determines the permission value:
7 = rwx
6 = rw-
5 = r-x
4 = r--
0 = ---

Examples:
700 = only the owner has full access
755 = owner has full access, others can read and enter
644 = standard file permissions
770 = owner and group have full access, others have none
