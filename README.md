# usefull-tips


## delete git head(last repo)

- git reset HEAD^
- git push -u origin master --force
 
## Commit to repo
- git add -A || git add file
- git commit -m "Message"
- git push

## Commit to repo Branch
- git checkout -b your-new-branch
- git add <files>
- git commit -m <message>
- git push origin your-new-branch

# GCP
## Upload app engine
- gcloud config set myproject
- gcloud app deploy

## flag for scripts to ignore prompts(at the end) 
- - - quiet
