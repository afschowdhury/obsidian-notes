---
type: terminal
tags:fish, alias
category: tools
for_inteview: false
creation_date: 1970-01-01 06:00
modification_date: 2023-02-26 11:30
---


Current Folder : 




[[26-02-2023]]


### **Edit the fish configuration**

```shell
kate ~/.config/fish/config.fish
```


### to add alias : 

```shell

alias `command` = `your command`
```

### Example 

```
function ac
    git add .
    git commit -m "add all and commit"
end


alias g='git'
alias gst='git status'
alias 'rs' ='python main.py'
```
