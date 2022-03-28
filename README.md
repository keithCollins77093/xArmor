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
