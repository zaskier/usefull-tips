# usefull-tips

 #GIT
## Commit to repo
- git add -A || git add <files>
- git commit -m "Message"
- git push
 
## Git multibranch project typical comands
- git commit -m <message>
- git push origin your-new-branch
 - git checkout <branch>//switch branches
 - git pull REMOTE-NAME BRANCH-NAME //Pull from specific branch(REFSPEC specifies which refs to fetch and which local refs to update)
 - git merge // join 2 histories together
 - git rebase -reaply changes on top of another repo
 
 
## delete git head(last repo)

- git reset HEAD^
- git reset --hard HEAD~2
- git push -u origin master --force
 
## Check repository

- git checkout 

## Switch terminal account
- git config -- global user.email "your@email.xx"

# GCP
## Upload app engine
- gcloud config set project myproject
- gcloud app deploy

## flag for scripts to ignore prompts(at the end) 
- -- quiet
 
# NestJS
 ## CLI
 - nest g service cats
 - nest g resource //command not only generates all the NestJS building blocks (module, service, controller classes) but also an entity class, DTO classes as well as the testing (.spec) files.
 * --no-spec //no tests
 
 # Typeorm
 ```
npx ts-node node_modules/.bin/typeorm migration:generate -n
npx ts-node node_modules/.bin/typeorm migration:generate -n {name} 
npx ts-node node_modules/.bin/typeorm migration:run 
npx ts-node node_modules/.bin/typeorm migration:revert
npx ts-node node_modules/.bin/typeorm migration:generate -c seed -n  
 ```


## Logging filter example
```
 resource.type="gae_app"
 resource.labels.module_id="default"
 logName="project/project_id/logs/stderr" 
```
## gShell delete project with liens
```
gcloud projects delete {project_id} 
gcloud alpha resource-manager liens list
gcloud alpha resource-manager liens delete {selected lien} 



```


# NPM
## remove proxy setting
- npm config rm http-proxy
- npm config rm proxy

# CMD
## windows account details
- net user {username} /DOMAIN

