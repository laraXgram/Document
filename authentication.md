# Authentication

### Check Status

- If the specified person is the admin of the group, it returns true

```php
Auth::isChatAdmin(int|string|null $user_id, int|string|null $chat_id)

// Helper
isChatAdmin()
```

---

- If the specified person is the creator of the group, it returns true

```php
Auth::isChatCreator(int|string|null $user_id, int|string|null $chat_id)

// Helper
isChatCreator()
```

---

- If the specified person is the member of the group, it returns true

```php
Auth::isChatMember(int|string|null $user_id, int|string|null $chat_id)

// Helper
isChatMember()
```

---

- If the specified person is the kicked of the group, it returns true

```php
Auth::iskicked(int|string|null $user_id, int|string|null $chat_id)

// Helper
iskicked()
```

---

- If the specified person is the restricted of the group, it returns true

```php
Auth::isRestricted(int|string|null $user_id, int|string|null $chat_id)

// Helper
isRestricted()
```

---

- If the specified person is the left of the group, it returns true

```php
Auth::isLeft(int|string|null $user_id, int|string|null $chat_id)

// Helper
isLeft()
```

---

- If the specified person is the admin of the bot, it returns true

```php
Auth::isBotAdmin(int|string|null $user_id, int|string|null $chat_id)

// Helper
isBotAdmin()
```

---

- If the specified person is the owner of the bot, it returns true

```php
Auth::isBotOwner(int|string|null $user_id, int|string|null $chat_id)

// Helper
isBotOwner()
```

---

* Bot administrators and bot owners are those who are not admins or group owners, but have specific access to use the
  bot.
* If the entries are null, the sender of the message is considered to be in the current group.

> **Note:**
>1. **The admin and owner of the bot are authenticate based on the default database structure, whose migration is
    present in the project by default.**
>2. **Follow Laragram rules for proper functioning, otherwise you must use personal authentication system.**
>3. **In the future, we will try to make this dynamic.**

> - After you make a group member the bot admin or bot owner, you must save it in the database.
> - You can do this easily with the following functions:

### Role

* Add new BotAdmin

```php
Role::addBotAdmin(int|string|null $user_id, int|string|null $chat_id)

// Helper
addBotAdmin()
```

---

* Add new BotOwner

```php
Role::addBotOwner(int|string|null $user_id, int|string|null $chat_id)

// Helper
addBotOwner()
```

---

* Remove BotAdmin or BotOwner

```php
Role::removeRole(int|string|null $user_id, int|string|null $chat_id)

// Helper
removeRole()
```

---

### Level

* Set User Level

```php
Level::setLevel(string|int $level, int|string|null $user_id, int|string|null $chat_id)

// Helper
setLevel()
```

---

* Remove User Level

```php
Level::removeLevel(int|string|null $user_id, int|string|null $chat_id)

// Helper
removeLevel()
```
---
#### **This structure works based on Eloquent, so install Eloquent first**
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
### [⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)