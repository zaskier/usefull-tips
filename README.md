# usefull-tips

 # GIT

## Git multibranch project typical comands
```
- git clone --branch <branchname> <project clone url>
- git commit -m <message>
- git push origin your-new-branch
 - git checkout <branch>//check branch or switch branch
 - git pull REMOTE-NAME BRANCH-NAME //Pull from specific branch(REFSPEC specifies which refs to fetch and which local refs to update)
 - git merge // join 2 histories together
 - git rebase -reaply changes on top of another repo
 - git fetch --prune //sync with current repo version

 ```
 
 ## Commit to repo
 ```
- git add -A || git add <files>
- git commit -m "Message"
- git push
 ```
 
 
## delete git head(last repo)
```
- git reset HEAD^
- git reset --hard HEAD~2
- git push -u origin master --force
 ```

## Switch terminal account
 ```
- git config -- global user.email "your@email.xx"
```
# GCP
## Upload app engine
 ```
- gcloud config set project myproject
- gcloud app deploy
 ```

## flag for scripts to ignore prompts(at the end) 
 ```
- -- quiet
 ```
 
 ## Logging filter example
```
 resource.type="gae_app"
 resource.labels.module_id="default"
 logName="project/project_id/logs/stderr" 
 timestamp>="2022-07-01T20:00:00.000Z"
 timestamp<"2022-07-13T21:00:00.000Z"
```

## Firebase
```
// npm install -g firebase-tools
- firebase login 
- firebase projects:list
- firebase init
- firebase serve
- firebase deploy
```

 
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

## gShell delete project with liens
```
gcloud projects delete {project_id} 
gcloud alpha resource-manager liens list
gcloud alpha resource-manager liens delete {selected lien} 

```


# NPM
## remove proxy setting
```
- npm config rm http-proxy
- npm config rm proxy
```
## tests
```
- npm run tests:watch //then 'p' for regex to filter file name
```
# NODE
```
- nvm install lts/fermium 
/* lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.7 (-> N/A)
lts/fermium -> v14.18.2 (-> N/A)
lts/gallium -> v16.13.1 */
```
# CMD
## windows account details
```
- net user {username} /DOMAIN
```

# MAC OS
## kill port
```
lsof -i tcp:3000 
```

# Terraform 
```
- terraform init 
- terraform plan  
- terraform apply 
- echo google_sql_database_instance.backend_sql.private_ip_address | terraform console //to check on local machine cloud resources values
``` 
# Docker 
```
- docker system prune // will remove all volumes that are not used by at least one container.
- docker build -t react-docker:1.0.0-dev .   
- docker run --rm -it --name web -p 3000:3000 react-docker:1.0.0-dev   
```
# Docker GCP
```
- gcloud auth configure-docker
- sudo docker tag {imagename}  gcr.io/{projectname}/{container}
- docker push gcr.io/{projectname}/{container}
```


