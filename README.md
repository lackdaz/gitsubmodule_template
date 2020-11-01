# The Ultimate Checklist for git submodules (GSM)

## Cloning a repository with GSM
To clone the repository with the gitsubmodules:
- `git clone --recursive [URL to Git repo]`

To clone the GSM in (if you missed the previous command):
- `git submodule update --init --recursive`

To add GSM:
- `git submodule add -b <main> --name <name-of-GSM> <path-to-github-url> <path-to-create-directory>`  
e.g:  
`git submodule add -b main --name cv_utils git@github.com:lackdaz/cv_utils.git lib_cv_utils`

To delete GSM:


