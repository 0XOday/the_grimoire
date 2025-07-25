The kernel is the software component that provides the core set of operating system functions. These include features for managing system hardware and for communicating between software and hardware. A distribution or distro is the Linux Kernel plus a distinctive type of package manager and software repository with a selection of customizable shells, utilities, and applications. Distros also have either community-supported or commercial licensing and support options.

*Shells and Terminals*
The shell provides a command environment by which a user can operate the OS and applications. Many shell programs are avaliable to use with Linux, notably bash, zsh and ksh. These shells expose the same core command set but are distinguished by support for features such as command history, tab completion, command spelling correction or syntax highlighting.

Many Linux Distros are deployed with desktop environment. The boot process launches a terminal user interface connected to the default shell command interpreter. The terminal and shell are connected by a teletype (tty) device that handles text input and output in separate streams:

* stdin (0) takes the users key board input and writes it as data to the tty device for processing by the shell's command interpreter.
* stdout (1) reads data generated by the shell from the tty device and displays it though the terminal.
* stderr(2) carries error information 

Working at a terminal is referred to as using a shell interactively. Non-interactive use means the shell reads commands from a scripts file.

*Desktop Environments*
Linux distros designed for use as client PC's typically load a graphical desktop environment at startup. The graphical environment is driven by an open-source version of the X Window Display system called Xorg (or just X)