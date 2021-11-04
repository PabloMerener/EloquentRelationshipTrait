# EloquentRelationshipTrait

Get eloquent relationships in your Laravel projects.

Implement EloquentRelationshipTrait in your models:
```
<?php

namespace App;

use Illuminate\Contracts\Auth\MustVerifyEmail;
use Illuminate\Foundation\Auth\User as Authenticatable;
use Illuminate\Notifications\Notifiable;
use Laravel\Passport\HasApiTokens;
use App\Traits\EloquentRelationshipTrait;

class User extends Authenticatable
{
    use Notifiable, HasApiTokens, EloquentRelationshipTrait;
```

Implementing EloquentRelationshipTrait in User model
```
<?php

namespace App;

use Illuminate\Contracts\Auth\MustVerifyEmail;
use Illuminate\Foundation\Auth\User as Authenticatable;
use Illuminate\Notifications\Notifiable;
use Laravel\Passport\HasApiTokens;
use App\Traits\EloquentRelationshipTrait;

class User extends Authenticatable
{
    use Notifiable, HasApiTokens, EloquentRelationshipTrait;
```

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
