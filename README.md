# [GindaChen Blog](https://gindachen.github.io)


## How to install



Useful script when in trouble of git submodule:
```bash
# Delete the submodule entry from .gitmodules file:
# [submodule "path/to/submodule"]
#     path = path/to/submodule
#     url = https://github.com/user/repo.git

# Stage the .gitmodules changes:
git add .gitmodules

# Delete the submodule entry from `.git/config`

# Remove submodule files from working tree and index. 
# Note: this has not removed your local version.
git rm --cached path/to/submodule

# Optionally, remove your local submodule files:
rm -rf path/to/submodule

# Commit the changes:
git commit -m "Removed submodule <name>"


# Add submodule
git submodule add --depth=1 https://github.com/GindaChen/hugo-PaperModX.git themes/PaperMod
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
```

