# KNEX
## knex CLI

 ```
 - knex init
 - knex init -x ts
 - knex migrate:make --stub 
 - knex migrate:latest
 - knex migrate:up
 - knex migrate:rollback
 - knex seed:make seed_name
 - knex seed:run
 - knex seed:run --specific=seed-filename.js --specific=another-seed-filename.js
 ```
## to remember
 ```
knex.raw(`select * from foo where id = ${id}`) // NEVER DO THIS 
 ```

 # TypeORM
 ## typeORM CLI
  ```
 - typeorm entity:create path-to-entity-dir/entity
 - typeorm migration:generate -n
 - typeorm migration:create -n
 - typeorm migration:run
 - typeorm migration:revert
 - typeorm migration:show
 - typeorm schema:sync
 - typeorm query "SELECT * FROM USERS"
   ```
## typeORM scripts
  ```
    "typeorm": "ts-node --transpile-only -r tsconfig-paths/register ./node_modules/typeorm/cli.js -f ./database/ormconfig.ts",
    "seeder": "ts-node --transpile-only -r tsconfig-paths/register ./node_modules/typeorm-seeding/dist/cli.js -r ./database",
    "seed:config": "yarn seeder config",
    "seed:run": "yarn seeder seed",
    "setup": "yarn migration:run && yarn seed:config && yarn seed:run"
  ```
