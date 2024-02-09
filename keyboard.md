# Keyboard Builder

* Simple use
```php
$keyboard = Keyboard::inlineKeyboardMarkup(
    Make::row(
        Make::col('btn1', callback_data: '1'),
        Make::col('btn2', url: 'https://google.com')
    ),
    Make::row(
        Make::col('btn3', web_app: []),
        Make::col('btn4', switch_inline_query_current_chat: 'test')
    )
    // etc...
);
```

* With Helper:

```php
 $keyboard = inlineKeyboardMarkup(
    row(
        col('btn1', callback_data: '1'),
        col('btn2', url: 'https://google.com')
    ),
    row(
        col('btn3', web_app: []),
        col('btn4', switch_inline_query_current_chat: 'test')
    )
    // etc...
);
```
---
### [⬅️ Return to home](https://github.com/laraXgram/Document/readme.md)