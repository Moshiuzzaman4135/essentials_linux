# Alias
Rename `alias` file to `.alias` to make it invisible 
Add necessary aliases in the file to create alias commands
Add the alias file in `~/.bashrc` file by writing
```
# Adding alias file
if [ -f ~/.aliases ]; then
    . ~/.aliases
fi
```