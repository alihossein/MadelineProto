---
title: account.updateProfile
description: account.updateProfile parameters, return type and example
---
## Method: account.updateProfile  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|first\_name|[string](../types/string.md) | Optional|
|last\_name|[string](../types/string.md) | Optional|
|about|[string](../types/string.md) | Optional|


### Return type: [User](../types/User.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $MadelineProto->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$User = $MadelineProto->account->updateProfile(['first_name' => 'string', 'last_name' => 'string', 'about' => 'string', ]);
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - account.updateProfile
* params - `{"first_name": "string", "last_name": "string", "about": "string", }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/account.updateProfile`

Parameters:

first_name - Json encoded string
last_name - Json encoded string
about - Json encoded string



Or, if you're into Lua:

```
User = account.updateProfile({first_name='string', last_name='string', about='string', })
```

