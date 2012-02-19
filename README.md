# PW Textformatter: Query Records

ProcessWire Textformatter module, that adds record parsing to your textarea. Each line is a separate record, that gets parsed with ProcessWire's Query parsing module. This allows you to enter your small structures in natural language, store them in one field and have them returned as an array of objects.

---

## Example

### Field content

    id=1, name=ProcessWire, type="Very fast & simple CMS"
    id=2, name=Drupal, type="CMS favorized by many"
    id=3, name=Joomla, type="not so good CMS"

### PHP Code to retrieve this field

    <?php
        //assume fieldname 'listOfCms'
        $listOfCms = $page->listOfCms;
        foreach($listOfCms as $cms){
            var_dump($cms)
        }

### Returned Data

--- WiP ---

---

## Installation

--- WiP ---

## License

See LICENSE.md
      