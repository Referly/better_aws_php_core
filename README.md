# better_php_common
Core components used by multiple better aws php packages

## Usage

This package includes classes that are used across multiple better_xxx_php packages relating to AWS services.

## Classes

### Configuration

The configuration object. It is passed to the AWS client to configure it properly for use.

Usually one would call the ConfigurationFactory instead of initializing this class directly.


### ConfigurationFactory

Creates Configuration instances. Accepts an array of configuration key value pairs that are appropriately set
on the Configuration instance.

```php
$configFactory = new ConfigurationFactory;
$configuration = $configFactory->createConfiguration([
	'region' => 'us-east-1',
	'credentials' => [
		'key' => getenv('AWS_ACCESS_KEY_ID'),
		'secret' => getenv('AWS_SECRET_ACCESS_KEY'),
	],
]);
```

