# Anything Terminal

## helpful commands

* $ wget url
* loads file from url to current directory (perfect for .json-files)

* $ ps aux | grep fsck
* to my understanding: gives all current processes that contain fsck in the naming
* usefull when a ext. drive might be blocked by fsck after beeing plugged in. Just kill the given process using $ sudo kill (-9 if neccessary)
* ps = process status
* a = show processes for all users
* u = display the process's user/owner
* x = also show processes not attached to a terminal  

## git
* git log -S 'any string' --source --all path/to/file.js
* returns all commits, that contain changes with the given string in this ifile

## functions for ~/.bashrc
* -> run $ source .bashrc after modification for changes to take effect

* function g() { open "https://www.google.com/search?q=$1" ; };
* opens a new tab and searches google for given query
* i.e. $ g weather berlin 

## alisases

* alias simulator="open /Applications/Xcode.app/Contents/Developer/Applications/Simulator.app"
* open iPhone simulator

* alias emulator="cd ~/Library/Android/sdk/emulator && ./emulator -avd Pixel_XL_API_29"
* open Android emulator
