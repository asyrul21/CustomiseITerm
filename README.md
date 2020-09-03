# How to MOD UP your iTERM 2

1. Follow this instruction from [here](https://www.freecodecamp.org/news/jazz-up-your-zsh-terminal-in-seven-steps-a-visual-guide-e81a8fd59a38/) to:

   - Install Homebrew if you havent
   - Install OH-MY-ZSH

2. Git clone this repo to home directory to:

   - Copy _.oh-my-zsh_ to _.oh-my-zsh_alt_ (but you have to update your _.zshrc_ later)
   - Install some plugins

3. In your _.zshrc_ insert this:

```bash
# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH
export PATH="/opt/anaconda3/bin:$PATH"
export PATH="/opt/apache-maven/bin:$PATH"
export PATH="$PATH:/Users/asyrulhafetzy/flutter/bin"

# Path to your oh-my-zsh installation.
# export ZSH="/Users/asyrulhafetzy/.oh-my-zsh"

export ZSH="/Users/asyrulhafetzy/OHMYZSH/.oh-my-zsh_alt"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="agnoster"

# Set list of themes to pick from when loading at random
# Setting this variable when ZSH_THEME=random will cause zsh to load
# a theme from this variable instead of looking in ~/.oh-my-zsh/themes/
# If set to an empty array, this variable will have no effect.
# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

# Uncomment the following line to use case-sensitive completion.
# CASE_SENSITIVE="true"

# Uncomment the following line to use hyphen-insensitive completion.
# Case-sensitive completion must be off. _ and - will be interchangeable.
# HYPHEN_INSENSITIVE="true"

# Uncomment the following line to disable bi-weekly auto-update checks.
# DISABLE_AUTO_UPDATE="true"

# Uncomment the following line to automatically update without prompting.
# DISABLE_UPDATE_PROMPT="true"

# Uncomment the following line to change how often to auto-update (in days).
# export UPDATE_ZSH_DAYS=13

# Uncomment the following line if pasting URLs and other text is messed up.
# DISABLE_MAGIC_FUNCTIONS=true

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to disable auto-setting terminal title.
# DISABLE_AUTO_TITLE="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
# COMPLETION_WAITING_DOTS="true"

# Uncomment the following line if you want to disable marking untracked files
# under VCS as dirty. This makes repository status check for large repositories
# much, much faster.
# DISABLE_UNTRACKED_FILES_DIRTY="true"

# Uncomment the following line if you want to change the command execution time
# stamp shown in the history command output.
# You can set one of the optional three formats:
# "mm/dd/yyyy"|"dd.mm.yyyy"|"yyyy-mm-dd"
# or set a custom format using the strftime function format specifications,
# see 'man strftime' for details.
# HIST_STAMPS="mm/dd/yyyy"

# Would you like to use another custom folder than $ZSH/custom?
# ZSH_CUSTOM=/path/to/new-custom-folder

# Which plugins would you like to load?
# Standard plugins can be found in ~/.oh-my-zsh/plugins/*
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(
	git
	zsh-syntax-highlighting
	zsh-autosuggestions
)

source $ZSH/oh-my-zsh.sh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"
alias jn="jupyter notebook"
alias uom="ssh w99766aa@kilburn.cs.man.ac.uk"

# below is to replace machine name to symbol
# change prompt
# prompt_segment() - Takes two arguments, background and foreground.

# https://github.com/agnoster/agnoster-zsh-theme/issues/39

prompt_context(){
    prompt_segment $CURRENT_FG default '⚡'
}


```

4. Within your _.oh-my-zsh_alt_, go to Themes and open Agoster theme file using editor. Update these sections:

```bash
# Dir: current working directory
# https://github.com/agnoster/agnoster-zsh-theme/issues/19
# https://medium.com/@shandou/how-to-shorten-zsh-prompt-oh-my-zsh-14185f3e7ab7
prompt_dir() {
  # prompt_segment blue $CURRENT_FG '%~'
  # prompt_segment blue $CURRENT_FG '⚙️  %2~'
  # prompt_segment blue $CURRENT_FG '💡  %2~'
  prompt_segment blue $CURRENT_FG '\u2699 %c'
}
```
