# Updates

`getData()`

`Message()`

`Chat()`

`MessageID()`

`ChatID()`

`UserID()`

`FirstName()`

`LastName()`

`Username()`

`ReplyToUserID()`

`ReplyToMessageID()`

`ReplyToMessageFromUserID()`

`FromID()`

`FromChatID()`

`BotUsername()`

`MessageFromGroup()`

`MessageFromGroupTitle()`

`Text()`

`Caption()`

`Entities()`

`Date()`

`Location()`

`Contact()`

`Game()`

`Poll()`

`Venue()`

`GetContactPhoneNumber()`

`Callback_Query()`

`Callback_ID()`

`Callback_Data()`

`Callback_Message()`

`Callback_ChatID()`

`Callback_FromID()`

`Inline_Query()`

`Dice()`

`DiceEmoji()`

`DiceValue()`

`NewChatMembers()`

`LeftChatMember()`

`UpdateID()`

`UpdateCount()`

`getUpdateType()`

---
* **The updates are not complete, if an update needs to be included, let the support know so that they can be added in the next versions.**
* If you need the update but it doesn't exist, you can temporarily add it to the project.
* To do this, follow the steps below :
  1. Open **Core/Request.php**
  2. Add a method like below and enter the desired update name instead of `UpdateName` and also enter the desired update indices instead of `three points` in the array.
```php
public function UpdateName()
{
    return $this->updates['...'];
}
```
---
### [⬅️ Return to home](https://github.com/laraXgram/Document/blob/v1.10/readme.md)