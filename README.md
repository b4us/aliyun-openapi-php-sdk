# Open API SDK for php developers

## Composer

We have released a new SDK that supports Composer and gradually stop maintenance this version. Welcome to the new SDK: [**Alibaba Cloud SDK for PHP**](https://github.com/aliyun/openapi-sdk-php)

## Requirements

- PHP 5.3+

## Build

- to run unit tests, you will have to configure aliyun-sdk.properties files in your user directory, and make sure your project has corresponding service enabled, eg. openmr.

## Example

```php
include_once '../aliyun-php-sdk-core/Config.php';
use Ecs\Request\V20140526 as Ecs;

$iClientProfile = DefaultProfile::getProfile("cn-hangzhou", "<your accessKey>", "<your accessSecret>");
$client = new DefaultAcsClient($iClientProfile);

$request = new Ecs\DescribeRegionsRequest();
$request->setMethod("GET");
$response = $client->getAcsResponse($request);
print_r($response);
```

## License

licensed under the [Apache License 2.0](License.md)
