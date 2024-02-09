# Config

### ENV
* APP
```dotenv
# Project name
APP_NAME=my_bot
```
---
* BOT
```dotenv
# Bot token
BOT_TOKEN=

# Project address in server (index.php file)
BOT_DOMAIN=

# Bot username
BOT_USERNAME=

# Bot User id
BOT_USERID=

# Bot api server endpoint
BOT_API_SERVER=https://api.telegram.org

# Local api server dir (If you run the api server)
BOT_API_SERVER_DIR=

# Local api server log file
BOT_API_SERVER_LOG_DIR=
```
---
* ACCOUNT
```dotenv
# Account api id for local api server
API_ID=

# Account api hash for local api server
API_HASH=
```
---
* SERVER
```dotenv
# LaraGram development server ip
SERVER_IP=127.0.0.1

# LaraGram development server port
SERVER_PORT=9000
```
---
* DATABASE
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
* OPENSWOOLE
```dotenv
# OpenSwoole server ip
OPENSWOOLE_IP=127.0.0.1

# OpenSwoole server port
OPENSWOOLE_PORT=9501
```
---
* REDIS
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

### AutoLoader

* By default, the files are loaded by Autoload Composer.
* If you cannot use composer for any reason, you can use LaraGram's dedicated autoloader.
* To do this, follow the steps below :
  1. Open **Bootstrap/Bootstrap.php**
  2. Uncomment line **30** -> `$this->classLoader();`
  3. You can also add desired namespaces to autoload in line **58** -> `$namespacePrefixes`

---
### SetWebhook
* Set the webhook only to the index.php file in the root of the project.
---
### [⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)