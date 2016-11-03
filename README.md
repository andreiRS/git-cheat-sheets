# Git Cheat Sheets

## Usefull commands
```
# List the number of lines written per author:
git ls-tree -r -z --name-only HEAD -- */*.c | xargs -0 -n1 git blame \
--line-porcelain HEAD |grep  "^author "|sort|uniq -c|sort -nr

# Preformated log
git log --color --graph \
--pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' \
--abbrev-commit

# Finding the most changed files in git
git log --pretty=format: --name-only | sort | uniq -c | sort -rg | head -10
git log --pretty=format: --name-only frontend ":(exclude)*generated*" ":(exclude)*swc*" | sort | uniq -c | sort -rg  > changes.txt
```

test
