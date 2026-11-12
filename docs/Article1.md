Option 1: GitHub web UI

Open the repo and go to the root (the repo’s main page)
Click Add file → Create new file
In the name box, type the folder name followed by / and a file name, e.g. api-tests/README.md
Click Commit changes

GitHub can’t hold empty folders, so a placeholder file is needed.
Option 2: Git CLI

bash
# From the repo root
mkdir api-tests ui-tests utils

# Git ignores empty folders, so add a placeholder
touch api-tests/.gitkeep ui-tests/.gitkeep utils/.gitkeep

git add .
git commit -m "Add root folders"
git push origin <branch-name>

Option 3: Create several nested folders at once

bash
mkdir -p tests/api tests/ui pages utils
touch tests/api/.gitkeep tests/ui/.gitkeep pages/.gitkeep utils/.gitkeep
git add .
git commit -m "Add folder structure"
git push

Notes:

.gitkeep is just a convention. Any file works, such as a README.md.
If the repo has branch protection, push to a feature branch and raise a PR.
