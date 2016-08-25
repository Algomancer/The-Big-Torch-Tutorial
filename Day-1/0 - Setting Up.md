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


## Development Workflow

