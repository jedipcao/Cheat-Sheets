# useful-scripts

## Git Commands

### General
Change User Name and Email

    git config --global user.name "Mona Lisa"
    git config --global user.email "email@example.com"

Remerber Username and Password

    git config --global credential.helper wincred

Disable autocrlf in Windows

    git config core.autocrlf false

SafeCRLF

    git config --global core.safecrlf true
    git config --global core.safecrlf false
    git config --global core.safecrlf warn

### Submodule
Add submodule

    git submodule add [URL to Git repo] [Target Directory]

To remove a submodule you need to:

- Delete the relevant section from the .gitmodules file.
- Stage the .gitmodules changes git add .gitmodules
- Delete the relevant section from .git/config.
- Run git rm --cached path_to_submodule (no trailing slash).
- Run rm -rf .git/modules/path_to_submodule (no trailing slash).
- Commit git commit -m "Removed submodule <name>"
- Delete the now untracked submodule files rm -rf path_to_submodule

### Commits
Revert a commit
