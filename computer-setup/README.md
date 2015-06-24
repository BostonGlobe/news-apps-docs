# Computer setup

A quick guide to getting your computer setup and ready to make graphics.

- Install Xcode (from App store)
- Install [brew](http://brew.sh/) (make sure you cd to /usr/local)

### Node
`brew install node`

Check that it worked: `node -v` and `npm -v`

### Gulp
`sudo npm install -g gulp` 

Breakdown:
- **sudo** = ask for password, gives admin rights
- **npm** = node package manager
- **-g** = globally (install for entire computer, not just for current directory)
- **gulp** = task runner (package that node is installing)

### Git
- `brew install git`
- `git config --global user.name "username"`
- `git config --global user.email "youremail@something.com"`