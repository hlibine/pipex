# pipex
![125/100](https://img.shields.io/badge/125%2F100-brightgreen)
## Description

pipex is a project at 42 that involves creating a simple program to mimic the functionality of the shell command `pipe` (`|`). The goal is to execute two commands in two separate processes and redirect the output of the first command as input to the second command.

## Base Features

- Implements basic shell functionality with pipes.
- Handles simple command execution in two processes.
- Supports input/output redirection.

## Bonus Functionality

The bonus part of pipex enhances the basic functionality with the following features:

- **Multiple Pipes**: Ability to use multiple pipes in succession (`cmd1 | cmd2 | cmd3 ...`), which enables complex command line data processing.
- **Here_doc**: Implements `here_doc` functionality to allow for inline data entry that can be used as input to the command chain.

## Compatibility & Size

![](https://img.shields.io/badge/WSL-0a97f5?style=for-the-badge&logo=linux&logoColor=white)
![](	https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white)

![](https://img.shields.io/github/languages/code-size/hlibine/pipex?color=5BCFFF)

## Usage 

To clone the repository use:
```bash
git clone https://github.com/hlibine/pipex.git
```
Compilation & cleanup:

- `make` : Compiles the standard code.
- `make bonus` : Compiles the bonus code.
- `make all` : Compiles both the standard and bonus code.
- `make clean` : Cleans up object files (.o).
- `make fclean` : Cleans up all files generated by running make, including the executable.
- `make re` : Does a make fclean followed by a make to recompile all the the code.

Example usage of standard pipex:
```bash
./pipex infile "ls -l" "wc -l" outfile
```
Example usage of pipex with bonus features:
```bash
./pipex infile "ls -l" "grep .c" "wc -l" outfile  # multiple pipes
./pipex here_doc LIMITER "cmd1" "cmd2" outfile    # here_doc
```
