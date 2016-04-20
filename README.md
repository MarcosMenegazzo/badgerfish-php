# BadgerFish-PHP

A PHP Library to transform XML into JSON and JSON into XML following the BadgerFish convention.

Forked from [jobywalker/Imperium-BadgerFish](https://github.com/jobywalker/Imperium-BadgerFish) in order to remove namespace and a minor improvement to XML exporting.


Usage:

```php
$json = '{ "anode": { "@xmlns": "http://anode.ns", "@id": 1, "child": { "@id": 10, "type": "anodes kid", "value": 123.45 } } }';

header("content-type: text/plain");
echo $json;
echo "\n\n";
echo BadgerFish::jsonToXML($json);
```
## Option(s)

### Does not export xml version tag

If you dont need the `<?xml>` tag starting your output, just do:

```php
$xml = BadgerFish::jsonToXML($json, false);
```

The second argument controls the ouput of `<?xml>` tag.


## References

* [http://www.sklar.com/badgerfish/](http://www.sklar.com/badgerfish/)
* [JSON and XML Conversion](http://wiki.open311.org/JSON_and_XML_Conversion/)
