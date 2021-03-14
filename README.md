# Copy Files From Anywhere ( aka 'clone' )

## Introduction
Copy Files From Anywhere ( aka 'clone' ) is a lightweight BASH script which copies files/subfolders from a predefined source to whichever directory the clone command is being called from. Perfect for getting "Boilerplate" or template-type files into new projects. 

### Why clone?
Clone was built because I often use a similar file set up for new scripting projects. Rather than spending time setting up my index.html, styles.css and scripts.js; I decided to pour way more time into this project so that I don't ever have to do it again. 😄
Realistically though, it can be used for any file(s) which you need frequently make copies of.   

### Will clone maintain the folder structure of my template files?
Yes.

### What if I have multiple sets of files that I want to copy?
Clone includes an option to choose an alternate source folder at runtime.

## One time Setup - Important, read carefully! 
Prior to using clone, you will need to do some basic setup steps

1. Go to your local home folder:
$ cd ~

2. Check to see if you have a local /bin folder:
```
$ ls -la
```

3. If /bin is not in the output, create it (otherwise skip this step):
```
$ mkdir bin
```

4. Open or create .bash_profile in vim:
```
$ vim .bash_profile
```

5. Check the file to see if it includes the following text:
PATH=~/bin:$PATH

6. If the file already includes that line, quit vim ( then skip to step 7 ):
```
:q!
```

6a. Otherwise, do the following:
- Switch to insert mode by pressing the 'i' key
- Paste or type in the following text: 
```
PATH=~/bin:$PATH
```
- Get out of insert mode by pressing the 'Esc' key.
- Write Quit vim:
```
:wq!
```

7. copy 'clone' into your bin folder:
```
$ cp /someDir/clone ~/bin/clone
```
* ( Where '/someDir/' = the folder which currently containes the 'clone' file )

8. Run clone once (from anywhere) to set up the initial file structure
$ clone

### Now you have a ~/templates/default folder that you can use.
- To add 'clone'-able files/folders, just add them to the ~/templates/default folder as normal
- Likewise you can delete unwanted files/folders as normal
- If you want to have alternate cloneable folders, create those folders under ~/templates instead and put what you want in there

## Using clone 
1. cd into whichever folder you want to copy your template files into
2. To clone files from the /default folder, call the clone command without any parameters:
```
$ clone
```
2a. Or, to clone an alternate folder, call the clone command with the alternate folder name as a parameter:
```
$ clone /some_other_folder
```
* If you forget to start the alternate folder name with '/', don't worry; the script will put it in for you.

### Assuming that you had files/sub-folders in your source folder to copy, they will recursively copy into wherever you called the script from.



## Author
Jon Spencer (2021)
