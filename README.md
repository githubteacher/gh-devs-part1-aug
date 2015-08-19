# gh-devs-part1-aug
Class Repository for GH for Developers Part 1 - August 2015

## To show branch name in command prompt

Add the following to your .bashrc file:

```bash

# add branch to bash prompt
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\w\[\033[36m\]\$(parse_git_branch) \[\033[00m\] > "

```
