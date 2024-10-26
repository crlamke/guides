If you're encountering problems with partitions filling up, this guide can help you find the cause of the problem and come up with a solution.

Note: You may need to run these commands with sudo. If you get a permission denied when running a command, try running with sudo.

#To find the largest files in a directory

ls -lhSr  - The ls command lists the contents of a directory. The ‘l’ option provides a long/detailed listing. The ‘h’ option lists sizes in human-readable format. The ‘S’ option sorts by size. The ‘r’ option reverses the sort by size so the largest files are at the bottom.

Useful example – ls -lhSr /var/log will list the size of files in the /var/log directory, sorted by size so the largest files are at the bottom of the list.


#To check the status of disk storage

df -kh – The df command displays the details of all partitions mounted to a machine, including allocated size and how much space is free. The ‘k’ option lists the size of storage in blocks of 1KB. The ‘h’ option lists sizes in human-readable format.

Useful example – df -kf will list the free and used space in all partitions on a machine.


#To find the largest files in a directory

du -sh – The du command displays the size of files and directories. The ‘s’ option prints a summary/total size. The ‘h’ option lists sizes in human-readable format.

Useful example – du -sh /var/log/* will list the size of all files and directories in the /var/log directory.
Useful example 2 – du -sh /var/log/* |grep -e "[0-9]M" will list the size of all files and directories in the /var/log directory and filter out anything less than 1MB in size since you probably don’t care about those, depending on your use case.
