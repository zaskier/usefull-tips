# usefull-tips

 # GIT

## Git multibranch project typical comands
```
- git clone --branch <branchname> <project clone url>
- git pull origin <branchname>
- git commit -m <message>
- git push origin your-new-branch
 - git checkout <branch>//check branch or switch branch
 - git pull REMOTE-NAME BRANCH-NAME //Pull from specific branch(REFSPEC specifies which refs to fetch and which local refs to update)
 - git merge // join 2 histories together
 - git rebase -reaply changes on top of another repo
 - git reset --merge // move the branch pointer to a previous commit
 - git fetch --prune //sync with current repo version
 ```
 ## Git flow default init test
 ```
 - git flow init //only local
 - git push --set-upstream origin development
 - git flow feature start feature_branch
 - touch feature.html
 - git add .
 - git commit -m 'feature complete'
 - git flow feature finish feature_branch
 - git push origin
 - git flow release start '0.1.0'
 - git push --set-upstream origin release/0.1.0
 - touch release-fix.html
 - git add . 
 - git commit -m 'release fix'
 - git push origin
 - git flow release finish '0.1.'
 - git push origin 
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
  ```
 - nest generate <schematic> <name> [options] //nest generate res users
 - nest generate app //default app
 - nest generate app orders //ake default app monorepo
 - nest g app auth //monorepo module   
 - nest g library common //monorepo common library
 - nest g service cats
 - nest g resource //command not only generates all the NestJS building blocks (module, service, controller classes) but also an entity class, DTO classes as well as the testing (.spec) files.
 * --no-spec //no tests
  ```
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
## common flags
```
--legacy-peer-deps
 --save-dev
```
## tests
```
- npm run tests:watch //then 'p' for regex to filter file name
```
## others
```
- npm ci install //package.json depencencies
- npm 
- npm --v
- npm outdated //{-g} for globall packages
- npm update //{--save] to update package.json
- npm set registry  https://registry.mycorp.com
- npm adduser --registry  https://registry.mycorp.com
- npm login --registry https://registry.mycorp.com
- npm login --registry=https://registry.mycorp.com
- npm publish --registry http://verdaccio-dev.springpod.com --tag dev

npm unpublish <package-name>@<version>
```
## GraphQL
```
- npm run graphql
```
# LINT
```
npx eslint .eslintrc
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
## TS
```
- tsc //transpile all the file according to your tsconfig(usually prod).
- ts-node //start from the entry file and transpile the file step by step through the tree based on the import/export.(usually dev with --watch and nodemon).
```
# CMD
## windows account details
```
- net user {username} /DOMAIN
```

# LINUX
```
lsof -i tcp:3000 // kill port
cd <directory> 
cd - //go back
cd /mnt
ls
mkdir <name>
rmdir <name>
touch
nano
rm - r <name>
rm -rf <dirname>
fuser 3000/tcp 
fuser -k 8080/tcp
nano ".bashrc"  //ctrl+shift+x
wsl --shutdown //for windows WSL shuting
sudo chmod -R 777 node_modules 
sudo apt-get install <package name>//ubuntu
sudo apt install [package name] //debian
chmod -R 777 ./ //add permission fro files
```
## Connect using the Cloud SQL Auth proxy
```
wget https://dl.google.com/cloudsql/cloud_sql_proxy.linux.amd64 -O cloud_sql_proxy
	#Make the Cloud SQL Auth proxy executable:
chmod +x cloud_sql_proxy
	#For Linux environments, use this command to launch the Cloud SQL Auth proxy:
./cloud_sql_proxy -instances=INSTANCE_CONNECTION_NAME=tcp:0.0.0.0:1234
```

# Terraform 
```
- terraform init 
- terraform plan  
- terraform apply 
- echo google_sql_database_instance.backend_sql.private_ip_address | terraform console //to check on local machine cloud resources values
- terraform apply -var-file="terrafotn.test.tfvars"
``` 
# Docker 
```
- docker-compose up    
- docker-compose down  
- docker container ls -a
- docker image list 
- docker rmi <image-id>
- docker network ls
- docker build -t <service-name> .
- docker network inspect app-network
- docker container exec -it {{CONTAINER_ID}} npm run start
- docker system prune -a --volumes     
- docker system prune // will remove all volumes that are not used by at least one container.
- docker build -t react-docker:1.0.0-dev .   
- docker run --rm -it --name web -p 3000:3000 react-docker:1.0.0-dev   
- docker-compose up --build -V //in development to add new container
```
# Docker GCP
```
- gcloud auth configure-docker
- sudo docker tag {imagename}  gcr.io/{projectname}/{container}
- docker push gcr.io/{projectname}/{container}
```


