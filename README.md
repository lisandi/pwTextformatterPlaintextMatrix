# PW Textformatter: Query Records

ProcessWire Textformatter module, that adds record parsing to your textarea. Each line is a separate record, that gets parsed with ProcessWire's Query parsing module. This allows you to enter your small structures in natural language, store them in one field and have them returned as an array of objects.

---

## Example

### Field content

```
id=1, name=ProcessWire, type="Very fast & simple CMS"
id=2, name=Drupal, type="CMS favorized by many"
id=3, name=Joomla, type="not so good CMS"
```

### PHP Code to retrieve this field

```php
<?php
    //assume fieldname 'listOfCms'
    $listOfCms = $page->listOfCms;
    foreach($listOfCms as $cms){
        var_dump($cms)
    }
?>
```

### Returned Data

```

array(3) {
  [0]=>
  object(stdClass)#178 (3) {
    ["id"]=> string(1) "1"
    ["name"]=> string(11) "ProcessWire"
    ["type"]=> string(22) "Very fast & simple CMS"
  }
  [1]=>
  object(stdClass)#155 (3) {
    ["id"]=> string(1) "2"
    ["name"]=> string(6) "Drupal"
    ["type"]=> string(21) "CMS favorized by many"
  }
  [2]=>
  object(stdClass)#176 (3) {
    ["id"]=> string(1) "3"
    ["name"]=> string(6) "Joomla"
    ["type"]=> string(15) "not so good CMS"
  }
}
```

---

## Installation

--- WiP ---

## License

See LICENSE.md
      