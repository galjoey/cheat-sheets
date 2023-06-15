# Git Cheat Sheet

## To remove branches that do not have an equivalent remote branch

- First execute the command `git remote prune origing`.
- To prune local branches which do not have a remote equivalent in git using __powershell__ `git  branch -vva | Select-String -Pattern ': gone' | % { $_.ToString().Split(" ")[2] } | % { git branch -d $_ }  `
To prune local branches which do not have a remote equivalent in git using __bash__ `git branch -vva | grep ": gone" | awk '{print $1}' | xargs git branch -d`
