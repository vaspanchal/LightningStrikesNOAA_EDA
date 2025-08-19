## Git Tracking .gitignore file fixed
it was doing so coz .gitignore only ignores intracked files but the csv was already tracked and since it was very large in size, it caused issue

## fix
🔹 1. Remove the file from Git’s history (but keep it locally)

Run:

git rm --cached "archive/lightening strikes dataset.csv"

🔹 2. Commit the change
git commit -m "Remove large dataset file from repo"

Step 1: Install git filter-repo (recommended)

If you don’t have it:

Linux/macOS:

pip install git-filter-repo

git filter-repo --path "archive/lightening strikes dataset.csv" --invert-paths --force
git push origin main --force
