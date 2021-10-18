# usefull-tips


## delete git head(last repo)

- git reset HEAD^
- git reset --hard HEAD~2
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

## Check repository

- git checkout 

# GCP
## Upload app engine
- gcloud config set project myproject
- gcloud app deploy

## flag for scripts to ignore prompts(at the end) 
- -- quiet

## Logging filter example
```
 resource.type="gae_app"
 resource.labels.module_id="default"
 logName="project/project_id/logs/stderr" 
```


# NPM
## remove proxy setting
- npm config rm http-proxy
- npm config rm proxy

# CMD
## windows account details
- net user {username} /DOMAIN

