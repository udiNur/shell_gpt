# Install custom version
1. `cd ~/.pyenv/shims`
2. `cp sgpt sgpt_legacy`
3. `nano sgpt`
4. Paste the following code:
```bash
#!/usr/bin/env bash
set -e
[ -n "$PYENV_DEBUG" ] && set -x

program="${0##*/}"

export PYENV_ROOT="/Users/yehuda/.pyenv"
#exec "/opt/homebrew/opt/pyenv/bin/pyenv" exec "$program" "$@"
python ~/Projects/Python/shell_gpt/sgpt/app.py
```
