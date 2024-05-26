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
python /Users/yehuda/Projects/Python/shell_gpt/sgpt/app.py "$@"
```

# Other

## Config locations
- `nano ~/.config/shell_gpt/.sgptrc

## Conversation 

### Old

```
[DEFAULT]`
    CHAT_CACHE_PATH=/var/folders/xk/k84qfb0d41sgp8hp8k4jl3rh0000gn/T/chat_cache
CACHE_PATH=/var/folders/xk/k84qfb0d41sgp8hp8k4jl3rh0000gn/T/cache
CHAT_CACHE_LENGTH=100
```

### New

```
[DEFAULT]
CHAT_CACHE_PATH=/Users/yehuda/tmp/shellgpt/chat_cache
CACHE_PATH=/Users/yehuda/tmp/shellgpt/cache
CHAT_CACHE_LENGTH=1000
CACHE_LENGTH=1000
```