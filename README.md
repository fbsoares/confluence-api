# Atlassian Confluence PHP Client

## Installation

```json
"require": {
    "outdare/confluence-api":"1.0.1"
},
```

## Examples

### Creating Space
```php
<?php
$client = new \Outdare\Confluence\Client([
  'hostname' => 'my.atlassian.net',
  'user' => '<user>',
  'pass' => '<pass>'
]);

$space = new \Outdare\Confluence\Space($client);
$space->create("SPACEKEY", "My new space", "global", "It's my new space from API");
```

### Creating Page
```php
<?php
$page = new \Outdare\Confluence\Page($client);
$page->create("SPACEKEY", "My new page", "<p>Content for my page</p>");
```
## With some help

Thanks to Nate Good's package ***nategood/httpful*** that makes the use of cUrl pretty simple.
http://phphttpclient.com/

## Contributions

Feel free to contribute with ideas and completing the **todo.md** file

## Links

### Atlassian Confluence examples used as guideline
https://developer.atlassian.com/confcloud/confluence-rest-api-examples-39985294.html

### Atlassian Confluence API Docs for latest version
https://docs.atlassian.com/confluence/REST/latest/
