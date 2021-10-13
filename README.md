# EloquentRelationshipTrait

Finally with (new User)->getRelationships() or User::getRelationships() you will get:

```
[
 "notifications" => [
   "MorphMany",
   "Illuminate\Notifications\DatabaseNotification",
 ],
 "readNotifications" => [
   "MorphMany",
   "Illuminate\Notifications\DatabaseNotification",
 ],
 "unreadNotifications" => [
   "MorphMany",
   "Illuminate\Notifications\DatabaseNotification",
 ],
 "clients" => [
   "HasMany",
   "Laravel\Passport\Client",
 ],
 "tokens" => [
   "HasMany",
   "Laravel\Passport\Token",
 ],
]
```
