# About

`poty` is a shell function aimed to improve simplicity and efficiency while using [python-poetry](https://python-poetry.org/).

# Features

1. publish and push pipelines with a single command
2. always clean cache before adding a new package to avoid errors
3. load the venv quickly by directly finding it with `find`
4. execute Python scripts with its venv from any location
5. establishes a default venv to be used when poetry is not present

# Usage

```
USAGE
    poty [command] [options]

COMMANDS
    I, init ...................... Initialize the project for Poetry
    a, add [package] ............. Add a package with Poetry
    s, sh, shell ................. Activate the Poetry virtual environment
    v, venv [option] ............. Manage virtual environments
        rm, remove ............... Remove the current virtual environment
        n, new ................... Create a new virtual environment
    i, ins, install .............. Lock and install dependencies with Poetry
    P, pub, publish .............. Publish the package (default version type)
    p, push [commit message] ..... Commit and push changes to Git
    [path/to/script.py] .......... Run a Python script in its virtual environment
    poetry [command] ............. Execute any command of poetry
    help, --help, -h ............. Display this help message
```

# Install

1. Clone the repo:
```bash
git clone https://github.com/ximenesyuri/poty /path/to/your/favorite/location
```
2. Source `poty` in your `.bashrc`
```bash
echo  "source /path/to/your/favorite/location/poty" >> $HOME/.bashrc
```

Alternatively, to source `poty` only before executing it, use a local source:
```bash
echo "
    function poty() {
        source /path/to/your/favorite/location/poty && poty \"$@\"
    }
" >> $HOME/.bashrc
```

