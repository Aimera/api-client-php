Aimera platform API class and examples for PHP
===

## Event tracking example

This code prepares a call to Challenger server on event happened to a client identified by {client_id}:

```php
include_once 'challenger.client.php';

$chall = new Challenger('api.aimera.io');
$chall -> setKey('{secret_key}');
$chall -> setOwnerId({owner_id});
$chall -> setClientId({client_id});
$chall -> addParam('multiple', '{multiple}'); // Optional

if($chall -> trackEvent({event_id}) === false){
    // Error happened. Retry later.
}
```
