# OnenceWS

OnenceWS Http client for official 1nce rest api https://api.1nce.com

## Installation


```bash
composer require pipinstallpip/onencews:dev-master
```

Make sure that you have the PHP Module for `APCu` enabled and loaded. This is used to store the oauth2-token for subsequent requests, so we do not exhaust the ratelimit of the Endpoint. 
You can check this by running:
```sh
php -m | grep apcu
```
in your terminal.

## Usage

```php
use pipinstallpip\onencews\OnenceWS;

$clientId = 'yourclientid';
$clientSecret = 'yoursecretkey';

$api = new OnenceWS($clientId,$clientSecret);
$response = $api->getSimsList(); //return all sims
print_r($response);
```
### Class methods

- getSimsList
- getSimReachibility
- getSimUsage
- getSimRemainingData
- getSimRemainingSms
- getSmsList
- getSimInfo
- getSimStatus
- getSimEvents
- getSmsDetails
- sendSms
- resetSim
- changeSimState
- deleteSpecificSms


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)