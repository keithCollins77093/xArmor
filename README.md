# xArmor
Python program using ctypes and the apparmor library to provide CLI, API, and GUI power interface

Linux hypocrisy or fraud in security implementation:
                       (From comment online found doing security research a few years ago.)
           Example:    A read-only file, owned and controlled by the root user, which all of the configuration
                       files and many other system information files are, can be loaded into a text editor
                       or read using a Linux command, thereby producing a writable copy in memory.  With
                       your text editor, select all and copy, using ctrl-c if there is no menu option in the
                       standard Edit menu bar drop down menu.  Write the copy to a file which you own.
                       You can now edit it and make as many copies as you like.  Without root access,
                       the only use you are prevented from doing is writing it back to the original physical file.
                       Malware of any kind can read all of the configuration files, along with many other
                       critical system information files, and can execute access commands which do not require
                       sudo or root privileges to run, obtaining the output of them.
                       NO ROOT KIT IS REQUIRED FOR MALWARE TO FULLY EXPLORE YOUR COMPUTER.
                       The malware is also free to 'exfiltrate' the information obtained in inconspicuous
                       chunks over networks, including the ubiquitous Internet.
                       The Windows security model also allows this violation of read-only protection.

           This is criminally deliberate design, but none of the state governments and no branch of the
           federal government, that I know of, has investigated it, attempted to prosecute it, or tried
           to make a law requiring better security.
           YOU ARE NAKED AND UNDER A MICROSCOPE FACILITATED BY YOUR GOVERNMENTS. 


My Solution:


For read only copy protection to exist the operating system must implement the access and use meta data of files against any and all programs attempting to access or modify the file on any way.

This requires all installed packages, libraries, or any kind of runnable object to carry an identifier. Each software object identifier then requires a list of access rule objects for each file it is allowed to access. An inverse of this map, one for each file listing the access permissions of each runnable object, is also useful.

When a file access request is received by the O.S., the software object's identifier is received with it.  It's access rule list is checked to see if the file is on it and then whether the particular action requested is allowed.

Only the root administrative user may modify access lists or the access rule object itself.

When a file is read by an application, it's access list objects for the runnable objects in the application travels with the application' activities.  All file content buffers allowed for the programming language on the O.S. must implement this. Whenever the application tries to access any file to write or append to it, both files' rule lists and then entries are checked to determine if the action is allowed. 

If the software object can create a new file, only the content file's protections are relevant. Where a software object can create a new file can be limited to an express set of paths, each of which can have its own access rule software object list. 

