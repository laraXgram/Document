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
* Create an instance of Database Model:

```php
$message = new Message();
```

> Insert new data :
```php
$message->create([
    "id"     => 1,
    "status" => "active"
]);
```

> Conditional methode (where & orWhere) and get :
```php
// And
$message
    ->where('id', '=', '1')
    ->where('status', '=', 'active')
    // ...
    ->get();
```

```php
// Or
$message
    ->where('id', '=', '1')
    ->orWhere('status', '=', 'active')
    // ...
    ->get();
```

| Operator         | Operator |
|------------------|--------|
| =                | !=     |
| ==               | ===    |
| !==              | \>     |
| \>=               | <      |
| <=                |        |
**Note: = & == is same!**


> Update data :
```php
$message
    ->where('id', '=', '1')
    ->update('status', 'not active');
```

> Delete data :
```php
$message
    ->where('id', '=', '1')
    ->delete();
```

> Select first row of data:
```php
$message
    ->where('id', '=', '1')
    ->first();
```

> Select all data :
```php
$message->all();
```

> Count all data :
```php
$message->rowCount();
```

> Count selected data :
```php
$message
    ->where('id', '=', '1')
    ->count();
```

> Empty column :
```php
$message
    ->where('id', '=', '1')
    ->empty('status');
```

> Truncate all data :
```php
$message->truncate();
```
---
### Manage Model
```bash
php laragram make:jsonModel {model_name}
```
```bash
php laragram make:jsonModel User
```
---
### Model property

```php
// If the model name and json name are not the same, set the database name
protected string $database = 'Message';

// set fillable keys
protected array $fillable = ['status'];

// set guarded keys
protected array $guarded = ['id'];
```
---
### Manage Migration

* Create new table
```
php laragram make:jsonMigration {migration_name} --create={table_name}
```
```
php laragram make:jsonMigration create_users_table --create=users
```

* Edit table
```
php laragram make:jsonMigration {migration_name} --table={table_name}
```
```
php laragram make:jsonMigration edit_users_table --table=users
```

> Note:
> * Note that the names of the migrations should be similar to the example above
    >   `create_{table_name}_table`
    >   `edit_{table_name}_table`
> * The table_name must be plural (`users`, `addresses`)

---
### Work with migrations
>1. Build a migration
>2. Open the created file ( **path: Database/Json/Migrations/** )
>3. Start writing ( An example has been created for you )
* create table migrations :
```php
JsonSchema::create('column_name', function (JsonBlueprint $table) {
    // create column with string type
    $table->string('name');
    
    // create column with integer type
    $table->integer('name');
    
    // create column with array type
    $table->array('name');
    
    // create column with boolean type
    $table->boolean('name');
    
    // create column with double type
    $table->double('name');
    
    // create column with object type
    $table->object('name');
    
    // create column with any type
    $table->any('name');
    
    // make nullable column 
    $table->string('name')->nullable();
    
    // set default value for column
    $table->string('name')->default('default value');
    
    // make unique column
    $table->string('name')->unique();
    
    // make auto increment column
    $table->integer('id')->autoIncrement();
    
    // make auto increment column with start number
    $table->integer('id')->autoIncrement(100);
    
    // Note: autoIncrement must be an integer
});
```
* edit table migrations :
```php
JsonSchema::table('column_name', function (JsonBlueprint $table) {
    // All methods like create migrations
});
```
---
### Migrate

```
php laragram migrate:json
```
---
### [⬅️ Return to Databases](https://github.com/laraXgram/Document/blob/v1.10/databases.md)
### [⬅️⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)