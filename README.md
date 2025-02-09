# steeef

A customizable version of [steeef's] theme.

<img width="706" src="https://zimfw.github.io/images/prompts/steeef@2.png">

## What does it show?

- "`user` at `hostname` in `working directory`"
- Git branch name, or commit short hash when in ['detached HEAD' state].
  Also, unindexed, indexed, and untracked indicators, and an optional stashed
  indicator (must be customized, see below).
- Python [venv] indicator.
- Duration of the last command (optional, see below).
- Exit code of the last command (if non-zero).

## Settings

This theme can be customized with the following environment variables. If the
variable is not defined, the respective default value is used. There are default
colors for 256-color terminals (or otherwise).

| Variable        | Description             | Default value    |
| --------------- | ----------------------- | ---------------- |
| BRANCH_COLOR    | Git branch name color   | 81 (or cyan)     |
| HOST_COLOR      | Host name color         | 166 (or yellow)  |
| INDEXED_COLOR   | Git indexed color       | 118 (or green)   |
| INDEXED_IND     | Git indexed indicator   | ●                |
| PWD_COLOR       | Working directory color | 118 (or green)   |
| STASHED_COLOR   | Git stashed color       |                  |
| STASHED_IND     | Git stashed indicator   |                  |
| UNINDEXED_COLOR | Git unindexed color     | 166 (or yellow)  |
| UNINDEXED_IND   | Git unindexed indicator | ●                |
| UNTRACKED_COLOR | Git untracked color     | 161 (or red)     |
| UNTRACKED_IND   | Git untracked indicator | ●                |
| USER_COLOR      | User name color         | 135 (or magenta) |

The git stashed indicator will not be shown unless defined.

## Requirements

Requires Zim's [git-info] module to show git information.

- [steeef's](https://github.com/robbyrussell/oh-my-zsh/blob/master/themes/steeef.zsh-theme)
- ['detached HEAD' state](https://git-scm.com/docs/git-checkout#_detached_head)
- [venv](https://docs.python.org/3/library/venv.html)
- [git-info](https://github.com/zimfw/git-info)

### Optional

- [duration-info](https://github.com/zimfw/duration-info)
  - Enables showing the duration of the last command.

## Acknowledgements

- functionality for duration of command and exit code from [asciiship theme](https://github.com/zimfw/asciiship)
