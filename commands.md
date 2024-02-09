# Commands

### WebServer
* Start LaraGram Development Server
> If you are working on a local host, it is better to use this web server.
> Otherwise, Apache, Nginx, etc. web servers are a better option.
```bash
php laragram serve
```
---
* Start Local Api Server
```bash
php laragram start:apiserver
```
---
* Start LaraGram Development Server & Local Api Server
```bash
php laragram serve --api-server
```
---
* Start OpenSwoole Server
```bash
php laragram start:openswoole
```
```bash
php laragram serve --openswoole
```
---
* Start OpenSwoole Server & Local Api Server
```bash
php laragram serve --openswoole --api-server
```
---
### Manage Webhook
* Set Webhook
```bash
php laragram setWebhook
```
---
* Delete Webhook
```bash
php laragram deleteWebhook
```
---
### Manage Dependency
* Get Eloquent
```bash
php laragram get:eloqunet
```
---
* Remove Eloquent
```bash
php laragram remove:eloqunet
```
---
* Get AMPHP
```bash
php laragram get:amphp
```
---
* Remove AMPHP
```bash
php laragram remove:amphp
```
---
* Get Ext-Redis
```bash
php laragram get:redis
```
---
* Remove Ext-Redis
```bash
php laragram remove:redis
```
---
* Get OpenSwoole
```bash
php laragram get:openswoole
```
---
* Remove OpenSwoole
```bash
php laragram remove:openswoole
```
---
* Clean Vendor
  * Remove all extra dependencies
```bash
php laragram clear:vendor
```
---
### Manage Resource
* Create Resource
```bash
php laragram make:resource my-resource
```
---
* Delete Resource
```bash
php laragram remove:resource my-resource
```
---
### Manage API Controller
* Create Api Controller
```bash
php laragram make:api ApiName
```
---
* Delete Api Controller
```bash
php laragram remove:api ApiName
```
---
### Manage Model
* Create MySQL Model
```bash
php laragram make:model User
```
---
* Create Json Model
```bash
php laragram make:jsonModel User
```
---
### Manage Migrations
* Create MySQL migration for create table
```bash
php laragram make:migration {migration_name} --create={table_name}
```
---
* Create MySQL migration for edit table
```bash
php laragram make:migration {migration_name} --table={table_name}
```
---
* Create Json migration for create table
```bash
php laragram make:jsonMigration {migration_name} --create={table_name}
```
---
* Create Json migration for edit table
```bash
php laragram make:jsonMigration {migration_name} --table={table_name}
```
---
* Migrate MySQL migrations
```bash
php laragram migrate
```
---
* Migrate Json migrations
```bash
php laragram migrate:json
```
---
### [⬅️ Return to home](https://github.com/laraXgram/Document/readme.md)