# Eloquent

### Install Dependency
* Install Eloquent
```bash
php laragram get:eloquent
```
* Remove Eloquent
```bash
php laragram remove:eloquent
```
---

### Query
>* learn to work with Eloquent and Laravel query builder
   > Use the following links:
   >
   >  [Eloquent](https://laravel.com/docs/master/eloquent) -- [Queries](https://laravel.com/docs/master/queries)

---
### Model
```bash
php laragram make:model {model_name}
```
```bash
php laragram make:model User
```
---
### Migration

* Create new table
```
php laragram make:migration {migration_name} --create={table_name}
```
```
php laragram make:migration create_users_table --create=users
```

* Edit table
```
php laragram make:migration {migration_name} --table={table_name}
```
```
php laragram make:migration edit_users_table --table=users
```

> Note:
> * Note that the names of the migrations should be similar to the example above
    >   `create_{table_name}_table`
    >   `edit_{table_name}_table`
> * The table_name must be plural (`users`, `addresses`)
>
>
>1. Build a migration
>2. Open the created file ( **path: Database/Mysql/Migrations/** )
>3. Start writing ( An example has been created for you )
>
>* It is better to learn to work with Eloquent and Laravel query builder
   > Use the following links:
   >
   >  [Eloquent](https://laravel.com/docs/master/eloquent) -- [Queries](https://laravel.com/docs/master/queries)
---
### Migrate

```
php laragram migrate
```
---
### ENV Variable
```dotenv
# Database Power (on | off)
DB_POWER=on

# Database Driver
DB_DRIVER=mysql

# Database Hostname
DB_HOST=localhost

# Database Name
DB_DATABASE=laragram

# Database Username
DB_USERNAME=root

# Database Password
DB_PASSWORD=

# Database Charset
DB_CHARSET=utf8

# Database Collation
DB_COLLATION=utf8_general_ci

# Database Prefix
DB_PREFIX=
```
---
### [⬅️ Return to Databases](https://github.com/laraXgram/Document/blob/v1.10/databases.md)
### [⬅️⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)