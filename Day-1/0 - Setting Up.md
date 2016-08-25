# Setting Up

 Torch7 is extremely simple to set up, and works with Mac OS and Ubuntu 12 and above.

## Installation

```bash
# Be sure not to run this with sudo
git clone https://github.com/torch/distro.git ~/torch --recursive
cd ~/torch; bash install-deps;
./install.sh
```

Refresh your environment variables
```bash
# On Linux with bash
source ~/.bashrc
# On Linux with zsh
source ~/.zshrc
# On OSX or in Linux with none of the above.
source ~/.profile
```

LuaRocks is the package manager for Lua modules. You can browse lua packages over at [LuaRocks.org](https://luarocks.org/)
new packages can be installed with 
```luarocks install {PACKAGE_NAME}```

You can start the torch repl with ```th```

## Development Workflow

I have found the most productive workflow fuses a traditional text editor with the power of Jupyter (the interactive environment). The best fit I have found is to use [atom.io](https://atom.io/) with [Hydrogen](https://atom.io/packages/hydrogen) the hydrogen package lets you run your code directly in Atom using any Jupyter kernels you have installed. Ensure you have jupyter on your PATH  ```pip install jupyter``` 

![Hydrogen](http://i.imgur.com/mBDF0Lu.gif)
