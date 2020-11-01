# The Ultimate Checklist for git submodules (GSM)

## Cloning a repository with GSM
1. To clone the repository with the gitsubmodules:  
`git clone --recursive <URL to Git repo>`

1. To clone the GSM in (if you missed the previous command):  
`git submodule update --init --recursive`

## Adding a GSM to a current repository:
1. To add a gitsubmodule to a current directory, run:  
`git submodule add -b <main> --name <name_of_GSM> <path_to_github_url> <path_to_submodule>`  
e.g:  
`$ git submodule add -b main --name cv_utils git@github.com:lackdaz/cv_utils.git lib_cv_utils`

## Modify a GSM in a current repository:
1. Modify the `.gitmodules` files with a text editor:  
`vim .gitmodules`  
1. Then run:  
```git submodule sync```  
to update the `.git/config` files.


## Deleting GSM:
1. Delete the relevant GSM from the `.gitmodules` file with a text editor:  
`vim .gitmodules`
1. Delete the relevant line from `.git/config`:
` vim .git/config`
1. Remove the git cache:  
`git rm --cached <path_to_submodule>`
1. Commit and delete the untrack GSM:
`rm -rf <path_to_submodule>`  
`git add . && commit -m <removed_x_submodule>`

### References
---
1. [https://www.atlassian.com/git/articles/core-concept-workflows-and-tips](https://www.atlassian.com/git/articles/core-concept-workflows-and-tips)