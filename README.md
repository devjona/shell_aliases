```shell
# THESE ARE FOR .ZSH NOW...

# .zshrc:
# TO DISPLAY THE GIT BRANCH IN YOUR PROMPT:
function parse_git_branch() {
  git branch 2> /dev/null | sed -n -e 's/^\* \(.*\)/[\1]/p'
}

setopt PROMPT_SUBST
export PROMPT='%F{grey}%n%f %F{cyan}%~%f %F{green}$(parse_git_branch)%f %F{normal}$%f '%

# ---

# .zprofile
# ALIASES

# GENERAL TERMINAL
alias ll="ls -AlF"

# Z_PROFILE aliases
alias catprofile='cat ~/.zprofile'
alias vimprofile='vim ~/.zprofile'
alias reload-terminal='source ~/.zshrc'

# GIT ALIASES
alias gcm='git commit -m "'
alias amend='git commit --amend --no-edit'

alias gdf='git diff'
alias gdfsrc='git diff src/*'

alias gpl='git pull'
alias gplr='git pull --rebase'

alias gpsh='git push'
alias gpshf='git push --force-with-lease'
alias gpshup='git push --set-upstream origin'

alias gst='git status'
alias glg='git log'
alias gaa='git add .'
alias gco='git checkout'
alias gbr='git branch'

# GIT REBASING:
alias greb='git rebase'
alias grebd='git rebase origin/develop'
alias grebs='git rebase --skip'
alias grebc='git rebase --continue'
```
