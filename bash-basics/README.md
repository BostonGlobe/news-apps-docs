# Bash basics

A simple guide to get comfortable with the command line.

## Utility reference
- **pwd**: prints full path to the current directory
- **ls**: lists the contents of the current directory
- **cd [dir]**: Changes the current directory 
- **mkdir [dir]**: Makes a new directory

## 2 minute walkthrough
On a Mac, open up the Terminal program.

### Where are you?
Start by entering `pwd` and hit enter. This is a **utility**. `pwd` gives you the full directory path to where you currently are.

Now enter `ls`. This utility lists the contents of the current directory. Basically like taking a quick look around you.

### Navigate
Let's move around. First, see where you can move to by entering `ls -F`. the `-F` is a flag, which is basically an option for a utility. `-F` lists the contents but tells us which is a directory and which is a file. 

Now enter `cd` followed by the name of a directory (**the argument**) to change directory. For example, `cd projects` would move you into the `projects` folder. Then you can type `ls` again to see what is in there.

To go back up one level, `cd ..`.

To navigate multiple subdirectories, `cd projects/2015/map`.

### Autocomplete
If you start typing a directory or file name that exists and hit the `tab` key, it will autocomplete for you. If there is more than one possibilty they will be listed. Saves time.

### Make directory
To create a new directory, type `mkdir` and the name of the new directory. For example, `mkdir images`.


