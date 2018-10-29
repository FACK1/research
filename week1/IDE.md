


Integrated development environment
An integrated development environment (IDE) is a software application that provides comprehensive facilities to computer programmers for software development. An IDE normally consists of a source code editor, build automation tools, and a debugger. Most modern IDEs have intelligent code completion. Some IDEs, such as NetBeans and Eclipse, contain a compiler, interpreter, or both; others, such as SharpDevelop and Lazarus, do not. The boundary between an integrated development environment and other parts of the broader software development environment is not well-defined. Sometimes a version control system, or various tools to simplify the construction of a graphical user interface (GUI), are integrated. Many modern IDEs also have a class browser, an object browser, and a class hierarchy diagram, for use in object-oriented software development.

An integrated development environment (IDE) is a software suite that consolidates basic tools required to write and test software.

Developers use numerous tools throughout software code creation, building and testing. Development tools often include text editors, code libraries, compilers and test platforms. Without an IDE, a developer must select, deploy, integrate and manage all of these tools separately. An IDE brings many of those development-related tools together as a single framework, application or service. The integrated toolset is designed to simplify software development and can identify and minimize coding mistakes and typos.

commands
$ clear
$ cd /Applications/Utilities
$ ls
$ ls -l
$ ls -a
$ ls -la
$ ditto -V /old/work/ /new/work/
$ defaults write com.apple.screencapture disable-shadow -bool TRUE ...

change the prefrences
https://www.maketecheasier.com/customize-terminal-ubuntu/

make alias :
    Open your terminal emulator of choice. I favor iTerm 2 on the Mac. Macs and most Linux distributions come with one called “Terminal”. (I don’t know enough about Windows to be helpful there.)
    Type sudo nano ~/.bashrc in your BASH terminal window. This will open up the Nano text editor, which is my personal favorite for simple editing. You can use others. sudo is likely to be necessary for permission reasons, if it is and you use it, supply the password before going on to the next step.
    In that file, add the line: alias c=clear. Generally leave the rest of that file in place, you’re just wanting to add a line anywhere you want in the file.
    Save out the file by hitting Ctrl + O (in Nano).
    Quit Nano by hitting Ctrl + X (in Nano).
    Close the terminal window.
    Open a new terminal session, usually by hitting “New window” in your terminal emulator.
    Try out your alias by typing c and then hitting Enter. You should see your terminal clear.
