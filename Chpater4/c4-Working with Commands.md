# Working with Commands 

- type – Indicate how a command name is interpreted
- which – Display which executable program will be executed
- help – Get help for shell builtins
- man – Display a command's manual page
- apropos – Display a list of appropriate commands
- info – Display a command's info entry
- whatis – Display one-line manual page descriptions
- alias – Create an alias for a command


   ### Identifying Commands
   
   #### type – Display a Command's Type 
   `type command`   
   The type command is a shell builtin that displays the kind of command the shell will
   execute, given a particular command name.
   
   #### which – Display an Executable's Location    
  `which command`   
   To determine the exact location of a given executable, the which command is used.    
   
   ### Getting a Command's Documentation    
   
   #### help – Get Help for Shell Builtins  
   `help command`   
   bash has a built-in help facility available for each of the shell builtins. To use it, type
   “help” followed by the name of the shell builtin.    
   
   #### --help – Display Usage Information  
   `mkdir --help`   
   Many executable programs support a “--help” option that displays a description of the
       command's supported syntax and options.  
   
   #### man – Display a Program's Manual Page   
   `man program`    
   
   Man pages vary somewhat in format but generally contain the following:   
   - A title (the page’s name)  
   - A synopsis of the command's syntax 
   - A description of the command's purpose 
   - A listing and description of each of the command's options 
   
   _On most Linux systems, man uses less to display the manual page, so all of the familiar less commands work while displaying the page.    
   The “manual” that man displays is broken into sections and covers not only user commands but also system administration commands, programming interfaces, file formats
   and more._   
   
   ##### Man Page Organization
   | Section | contents |
   |---|---|
   | 1 | User commands |
   | 2 | Programming interfaces for kernel system calls |
   | 3 | Programming interfaces to the C library |
   | 4 | Special files such as device nodes and drivers |
   | 5 | File formats |
   | 6 | Games and amusements such as screen savers |
   | 7 | Miscellaneous |
   | 8 | System administration commands |   
   
   Without specifying a section number, we will always get the first instance of
   a match, probably in section 1. To specify a section number, we use man like this:   
   `man section search_term`    
   
   #### apropos – Display Appropriate Commands
   `apropos partiton`   
   The first field in each line of output is the name of the man page, and the second field
   shows the section. Note that the man command with the “-k” option performs the same
   function as **apropos**. 
   
   #### whatis – Display One-line Manual Page Descriptions
   `whatis ls`  
    The whatis program displays the name and a one-line description of a man page matching a specified keyword.
    
   #### info – Display a Program's Info Entry
   `info coreutils` 
   Info manuals are displayed with a reader program named, appropriately enough, info.
   Info pages are hyperlinked much like web pages.
   
   | Command | Action |
   |---|---|
   | ? | Display command help |
   | PgUp or Backspace | Display previous page |
   | PgDn or Space | Display next page |
   | n | Next - Display the next node |
   | p | Previous - Display the previous node |
   | u | Up - Display the parent node of the currently displayed node, usually a menu |
   | Enter | Follow the hyperlink at the cursor location |
   | q | Quit |
   
   README and Other Program Documentation Files
   Many software packages installed on our system have documentation files residing in the /usr/share/doc directory. Most of these are stored in plain text format and can be viewed with less. Some of the files are in HTML format and can be viewed with a web browser. We may encounter some files ending with a “.gz” extension. This indicates that they have been compressed with the gzip compression program. The gzip package includes a special version of less called zless that will display the contents of gzipcompressed text files.
   
   But before we start, we need to reveal a small command line trick. It's possible to put more than one command on a line by separating each command with a semicolon.  
   `command1; command2; command3... `
   
   `alias name='string'`    
   After the command alias, we give alias a name followed immediately (no whitespace allowed) by an equal sign, followed immediately by a quoted string containing the meaning to be assigned to the name. After we define our alias, we can use it anywhere the shell would expect a command.
   
   To remove an alias, the unalias command is used. 
   `unalias foo`