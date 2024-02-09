# Methods and Listener

# 👂 Listener

> - `on(array|string $message, callable $action)`
>- `onText(array|string $message, callable $action)`
>- `onCommand(array|string $command, callable $action)`
>- `onAnimation(callable $action, array|string $file_id = null)`
>- `onAudio(callable $action, array|string $file_id = null)`
>- `onDocument(callable $action, array|string $file_id = null)`
>- `onPhoto(callable $action, array|string $file_id = null)`
>- `onSticker(callable $action, array|string $file_id = null)`
>- `onVideo(callable $action, array|string $file_id = null)`
>- `onVideoNote(callable $action, array|string $file_id = null)`
>- `onVoice(callable $action, array|string $file_id = null)`
>- `onContact(callable $action)`
>- `onDice(callable $action, string|null $emoji = null, string|int|null $value = null)`
>- `onGame(callable $action)`
>- `onPoll(callable $action)`
>- `onVenue(callable $action)`
>- `onLocation(callable $action)`
>- `onNewChatMembers(callable $action)`
>- `onLeftChatMember(callable $action)`
>- `onNewChatTitle(callable $action)`
>- `onNewChatPhoto(callable $action)`
>- `onDeleteChatPhoto(callable $action)`
>- `onGroupChatCreated(callable $action)`
>- `onSuperGroupChatCreated(callable $action)`
>- `onMessageAutoDeleteTimerChanged(callable $action)`
>- `onMigrateToChatId(callable $action)`
>- `onMigrateFromChatId(callable $action)`
>- `onPinnedMessage(callable $action)`
>- `onInvoice(callable $action)`
>- `onSuccessfulPayment(callable $action)`
>- `onConnectedWebsite(callable $action)`
>- `onPassportData(callable $action)`
>- `onProximityAlertTriggered(callable $action)`
>- `onForumTopicCreated(callable $action)`
>- `onForumTopicEdited(callable $action)`
>- `onForumTopicClosed(callable $action)`
>- `onForumTopicReopened(callable $action)`
>- `onVideoChatScheduled(callable $action)`
>- `onVideoChatStarted(callable $action)`
>- `onVideoChatEnded(callable $action)`
>- `onVideoChatParticipantsInvited(callable $action)`
>- `onWebAppData(callable $action)`
>- `onMessage(callable $action);`
>- `onMessageType(string|array $type, callable $action);`
>- `onEditedMessage(callable $action);`
>- `onChannelPost(callable $action);`
>- `onEditedChannelPost(callable $action);`
>- `onInlineQuery(callable $action);`
>- `onChosenInlineResult(callable $action);`
>- `onCallbackQuery(callable $action);`
>- `onCallbackQueryData(string|array $pattern, callable $action);`
>- `onShippingQuery(callable $action);`
>- `onPreCheckoutQuery(callable $action);`
>- `onPollAnswer(callable $action);`
>- `onMyChatMember(callable $action);`
>- `onChatMember(callable $action);`
>- `onChatJoinRequest(callable $action);`
>- `onAny(callable $action);`
---

### Methods
* The methods are exactly the same as the telegram api methods.
### ⚙️ Usage
1. make a resource and open it --- **Path: `App/Resources`**
* Create Resource
```bash
php laragram make:resource my-resource
```
* Remove Resource
```bash
php laragram remove:resource my-resource
```

2. Create an instance of Bot()

```php
$bot = new Bot();
```

3. Start Coding

* Simple use
```php
$bot->onText('hello', function(Request $request){
  $request->sendMessage([
    'chat_id' => $request->ChatID(),
    'text'    => 'hi'
  ]);
});
```

* Use Variable

```php
$bot->onText('say {text}', function(Request $request, $text){
  $request->sendMessage([
    'chat_id' => $request->ChatID(),
    'text'    => $text
  ]);
});
```

* Pass Multiple Pattern

```php
$bot->onText(['hello', 'hay'], function(Request $request){
  $request->sendMessage([
    'chat_id' => $request->ChatID(),
    'text'    => 'hi'
  ]);
});
```

* Use Helper

```php
$bot->onText(['hello', 'hay'], function(){
  sendMessage([
    'chat_id' => ChatID(),
    'text'    => 'hi'
  ]);
});
```

### Change Request Method

  ##### Constant

| Type                             | Name                            | Int   |
|----------------------------------|---------------------------------|-------|
| Curl (Default)                   | `REQUEST_METHODE_CURL`          | `32`  |
| Parallel curl                    | `REQUEST_METHODE_PARALLEL_CURL` | `64`  |
| AMPHP                            | `REQUEST_METHODE_AMPHP`         | `128` |
| OpenSwoole ( Not available yet ) | `REQUEST_METHODE_OPENSWOOLE`    | `256` |

```php
$bot->onText(['hello', 'hay'], function(Request $request){
  $request->sendMessage([
    'chat_id' => $request->ChatID(),
    'text'    => 'hi'
  ], REQUEST_METHODE_PARALLEL_CURL);
});
```
---
### [⬅️⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)