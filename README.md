# PW Textformatter: Plaintext Matrix 1.0.0

Transform your textareas into matrixes: enter your records in plaintext – ProcessWire query syntax, and upon page loading, get your data back as array of objects with typed values!

---

## Example

### Field content

```
id=1, name=ProcessWire, type="Very fast & simple CMS"
id=2, name=Drupal, type="CMS, favorited by many"
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

1. Install module as usually (either download and copy into your `site/modules/` directory, or clone somewhere else and symlink this directory into your site **\***)
2. Create new textarea
3. Set Plaintext Matrix as Textformatter for the textarea
4. Use and be happy

* – If you are on a OS X, use absolute paths (as `/Users/adam/lib/.../module` instead of e.g. `./module` if you're in your modules directory) – otherwise you may run into 'too many redirects' problem.

## License

See LICENSE
      