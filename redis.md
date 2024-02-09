# Redis

### Install Dependency
* Install EXT-Redis
```bash
php laragram get:redis
```
* Remove EXT-Redis
```bash
php laragram remove:redis
```
---
### ⚙️ Usage

```php
// init Redis Server
$redis = PhpRedis::connect();

// set
$redis->set($key, $value);
$redis->set('foo', 'bar');

//get
$data = $redis->get($key));
$data = $redis->get('foo'));

// The rest of the methods are the same as the php redis client
```

* Pass Db name:

```php
// init Redis Server with db name
$redis = PhpRedis::connect('dbname');
```
---
### ENV Variable
```dotenv
# Redis server ip
REDIS_IP=127.0.0.1

# Redis server port
REDIS_PORT=6379

# Redis server username
REDIS_USER=

# Redis server password
REDIS_PASS=

# Redis server database name
REDIS_DB=9000
```
---
### [⬅️ Return to Databases](https://github.com/laraXgram/Document/databases.md)
### [⬅️⬅️ Return to home](https://github.com/laraXgram/Document/readme.md)
