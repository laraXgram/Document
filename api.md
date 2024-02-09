# API

1. Build an api controller
* make controller
```bash
php laragram make:api ApiName
```
* remove controller
```bash
php laragram remove:api ApiName
```

2. Open the created file ( path: **App/Controller/Api** )
3. Start writing

* API Controller
```php
namespace Bot\App\Controller\Api;

use Bot\Core\http\RegisterApi;

class DateTime extends RegisterApi
{
    public function time($country){
        // Request to api endpoint for get time
        return $time; // receive from api
    }
}
```

* Use Api In Resource File :
```php
$api = new Api();

//$api->api('APIName@MethodName', ...$parameters);
$api->api('DateTime@time', 'iran');

// Helper 
//api('APIName@MethodName', ...$parameters);
api('DateTime@time', 'iran')
```
---
### [⬅️ Return to home](https://github.com/laraXgram/Document/readme.md)
