# bash rc scripts meant for the XDG standard .config/ directory

## setup Eternal bash history.

```bash
# Eternal bash history.
# ---------------------
# Undocumented feature which sets the size to "unlimited".
# http://stackoverflow.com/questions/9457233/unlimited-bash-history
export HISTFILESIZE=
export HISTSIZE=
export HISTTIMEFORMAT="[%F %T] "
# Change the file location because certain bash sessions truncate .bash_history file upon close.
# http://superuser.com/questions/575479/bash-history-truncated-to-500-lines-on-each-login
export HISTFILE=~/.bash_eternal_history

# Force prompt to write history after every command.
# http://superuser.com/questions/20900/bash-history-loss
PROMPT_COMMAND="history -a; $PROMPT_COMMAND"
```

# what to add to .bashrc.. for now

```bash
# load bash rc from XDG location
export XDG_CONFIG_HOME="${XDG_CONFIG_HOME:-$HOME/.config}"
[ -s "$XDG_CONFIG_HOME/bash/rc" ] && source "$XDG_CONFIG_HOME/bash/rc"

```
