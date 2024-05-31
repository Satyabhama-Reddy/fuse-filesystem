# fuse-filesystem
Filesystem in Userspace

## INTRODUCTION TO FUSE
FUSE (Filesystem in Userspace) is a simple interface for userspace programs to export a virtual filesystem to the Linux kernel. Fuse also aims to provide a secure method for non privileged users to create and mount their own file system implementations. The FUSE system was originally part of AVFS, a filesystem implementation heavily influenced by the translator concept of the GNU Hurd. 

## OPERATION AND USES
To implement a new file system, a handler program linked to the supplied libfuse library needs to be written. The main purpose of this program is to specify how the file system is to respond to read/write/stat requests. The program is also used to mount the new file system. At the time the file system is mounted, the handler is registered with the kernel. If a user now issues read/write/stat requests for this newly mounted file system, the kernel forwards these IO-requests to the handler and then sends the handler's response back to the user.FUSE is particularly useful for writing virtual file systems.  
