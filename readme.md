```

Thes-MacBook-Air:Development associateinstructor$ mkdir vending
Thes-MacBook-Air:Development associateinstructor$ cd vending
Thes-MacBook-Air:vending associateinstructor$ touch readme.md
Thes-MacBook-Air:vending associateinstructor$ touch app.js
Thes-MacBook-Air:vending associateinstructor$ npm init --yes
Wrote to /Users/associateinstructor/Desktop/Development/vending/package.json:

{
  "name": "vending",
  "version": "1.0.0",
  "description": "",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}


Thes-MacBook-Air:vending associateinstructor$ npm install express mustache mustache-express express body-parser --save
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN vending@1.0.0 No description
npm WARN vending@1.0.0 No repository field.

+ mustache@2.3.0
+ body-parser@1.17.2
+ express@4.15.4
+ express@4.15.4
+ mustache-express@1.2.5
added 54 packages in 5.211s


   ╭─────────────────────────────────────╮
   │                                     │
   │   Update available 5.3.0 → 5.4.0    │
   │     Run npm i -g npm to update      │
   │                                     │
   ╰─────────────────────────────────────╯

Thes-MacBook-Air:vending associateinstructor$ gitignore node
Created .gitignore file for type Node :)
Thes-MacBook-Air:vending associateinstructor$ git init
Initialized empty Git repository in /Users/associateinstructor/Desktop/Development/vending/.git/
Thes-MacBook-Air:vending associateinstructor$ git add .
Thes-MacBook-Air:vending associateinstructor$ git commit -m"initial commit"
[master (root-commit) 901d691] initial commit
 Committer: Associate Instructor <associateinstructor@Thes-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 5 files changed, 479 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 app.js
 create mode 100644 package-lock.json
 create mode 100644 package.json
 create mode 100644 readme.md
Thes-MacBook-Air:vending associateinstructor$ git remote add origin https://github.com/shahzadkhan3iii7/sql-vending-machine.git
Thes-MacBook-Air:vending associateinstructor$ git push -u origin master
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 4.09 KiB | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/shahzadkhan3iii7/sql-vending-machine.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
Thes-MacBook-Air:vending associateinstructor$ atom .
Thes-MacBook-Air:vending associateinstructor$ npm install -g sequelize-cli
npm WARN deprecated minimatch@2.0.10: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
npm WARN deprecated minimatch@0.2.14: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
npm WARN deprecated graceful-fs@1.2.3: graceful-fs v3.0.0 and before will fail on node releases >= v7.0. Please update to graceful-fs@^4.0.0 as soon as possible. Use 'npm ls graceful-fs' to find it in the tree.
/usr/local/bin/sequelize -> /usr/local/lib/node_modules/sequelize-cli/bin/sequelize
+ sequelize-cli@2.8.0
updated 2 packages in 13.255s
Thes-MacBook-Air:vending associateinstructor$ npm install sequelize pg --save
npm WARN vending@1.0.0 No description
npm WARN vending@1.0.0 No repository field.

+ pg@7.3.0
+ sequelize@4.8.0
added 38 packages in 11.084s
Thes-MacBook-Air:vending associateinstructor$ sequelize init

Sequelize [Node: 8.1.4, CLI: 2.8.0, ORM: 4.8.0]

Created "config/config.json"
Successfully created migrations folder at "/Users/associateinstructor/Desktop/Development/vending/migrations".
Successfully created seeders folder at "/Users/associateinstructor/Desktop/Development/vending/seeders".
Successfully created models folder at "/Users/associateinstructor/Desktop/Development/vending/models".
Thes-MacBook-Air:vending associateinstructor$ whoami
associateinstructor
Thes-MacBook-Air:vending associateinstructor$ createdb
Thes-MacBook-Air:vending associateinstructor$ psql vendingdb
psql: FATAL:  database "vendingdb" does not exist
Thes-MacBook-Air:vending associateinstructor$ createdb vendingdb
Thes-MacBook-Air:vending associateinstructor$ psql
psql (9.6.4)
Type "help" for help.

associateinstructor=# \d
No relations found.
associateinstructor=# \q
Thes-MacBook-Air:vending associateinstructor$ createdb vendingdb
createdb: database creation failed: ERROR:  database "vendingdb" already exists
Thes-MacBook-Air:vending associateinstructor$ psql vendingdb
psql (9.6.4)
Type "help" for help.

vendingdb=# \d
No relations found.
vendingdb=# \q
Thes-MacBook-Air:vending associateinstructor$ sequelize db:migrate

Sequelize [Node: 8.1.4, CLI: 2.8.0, ORM: 4.8.0]

Loaded configuration file "config/config.json".
Using environment "development".
No migrations were executed, database schema was already up to date.
Thes-MacBook-Air:vending associateinstructor$ psql vendingdb
psql (9.6.4)
Type "help" for help.

vendingdb=# \d
                  List of relations
 Schema |     Name      | Type  |        Owner
--------+---------------+-------+---------------------
 public | SequelizeMeta | table | associateinstructor
(1 row)

vendingdb=# \q
Thes-MacBook-Air:vending associateinstructor$ sequelize model:create --name Item --attributes 'name:string cost:integer'

Sequelize [Node: 8.1.4, CLI: 2.8.0, ORM: 4.8.0]

Loaded configuration file "config/config.json".
Using environment "development".
Thes-MacBook-Air:vending associateinstructor$ psql vendingdb
psql (9.6.4)
Type "help" for help.

vendingdb=# \d
                  List of relations
 Schema |     Name      | Type  |        Owner
--------+---------------+-------+---------------------
 public | SequelizeMeta | table | associateinstructor
(1 row)

vendingdb=# \q
Thes-MacBook-Air:vending associateinstructor$ sequelize db:migrate

Sequelize [Node: 8.1.4, CLI: 2.8.0, ORM: 4.8.0]

Loaded configuration file "config/config.json".
Using environment "development".
== 20170905193236-create-item: migrating =======
== 20170905193236-create-item: migrated (0.103s)
Thes-MacBook-Air:vending associateinstructor$ psql vendingdb
psql (9.6.4)
Type "help" for help.

vendingdb=# \d
                    List of relations
 Schema |     Name      |   Type   |        Owner
--------+---------------+----------+---------------------
 public | Items         | table    | associateinstructor
 public | Items_id_seq  | sequence | associateinstructor
 public | SequelizeMeta | table    | associateinstructor
(3 rows)

vendingdb=# \q
Thes-MacBook-Air:vending associateinstructor$

```
