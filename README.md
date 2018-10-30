Aimera platform API class and examples for PHP
===

## Event tracking example

This code prepares a call to Challenger server on event happened to a client identified by {client_id}:

```php
include 'challenger.client.php';

$chall = new Challenger('api.aimera.io');
$chall -> setKey('{secret_key}');
$chall -> setOwnerId({owner_id});
$chall -> setClientId({client_id});
$chall -> addParam('multiple', '{multiple}'); // Optional
$resp = $chall -> trackEvent({event_id});

if($resp === false){
    // Error happened. Check is servers are not down.
}
```
