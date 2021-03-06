Setting up a very simple controller using pox. 

# Requirements and Environment
You need python. I have tested my code on Ubuntu 14.  

# Setup
0. You first need to clone pox repository:
`git clone https://github.com/noxrepo/pox.git`
0. Then switch into `/pox/` directory and clone this repository: 

  ```
  cd pox
  git clone https://github.com/Ehsan70/SDN.git
  ```
0. The repo is cloned into the folder SDN. But you need to copy of the files in the `/SDN/` into `/ext/`. Or you can simply delete `/ext/` and rename `/SDN/` to `ext`. It depends if you are already working on anything or not. I assume you are new, do the following:

  ```
  # in the pox directory
  rm -r ext/
  mv SDN/ ext/
  ```
0. So now you have the files setup. Make sure you have the files from this repo in `ext` directory. The reason for that is the fact that pox assumes external files are places in that directory. You can run a `MyTest` controller by exceuting: 

  ```
  # Move back to pox dir
  cd ..
  sudo ./pox.py MyTest
  ``` 

`pox.py` looks at ext directory and tries to find `MyTest.py`. Note that you should not put the `.py` in the command. You just need the command name. 

# Note 
At directory `pox/ext` you can make your own controler. This directory is not under version control for `pox`, so it makes a good place to put your own projects. Files of this repo should be placed in that dir. 
