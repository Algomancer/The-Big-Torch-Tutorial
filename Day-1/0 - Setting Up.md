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

I have found the most productive workflow fuses a traditional text editor with the power of Jupyter (the interactive environment). The best fit I have found is to use atom.io with [Hydrogen](https://atom.io/packages/hydrogen) the This package lets you run your code directly in Atom using any Jupyter kernels you have installed. Ensure you have jupyter on your PATH  ```pip install jupyter``` 

![](https://i.github-camo.com/72e6077d4293e44220f5a5c33a897d1394b49b2c/68747470733a2f2f636c6f75642e67697468756275736572636f6e74656e742e636f6d2f6173736574732f31333238353830382f31343539383737382f31636666316233322d303535342d313165362d383138312d3530343330376361366235362e676966)
