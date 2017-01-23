# MvcCore Extension - View Helper Line Breaks

[![Latest Stable Version](https://img.shields.io/badge/Stable-v3.1.0-brightgreen.svg?style=plastic)](https://github.com/mvccore/example-helloworld/releases)
[![License](https://img.shields.io/badge/Licence-BSD-brightgreen.svg?style=plastic)](https://github.com/mvccore/example-helloworld/blob/master/LICENCE.md)
![PHP Version](https://img.shields.io/badge/PHP->=5.3-brightgreen.svg?style=plastic)

View helper extension for processing any visible text content for non-line breaking spaces.
Spaces between digits like `9 999` are replaced into `9&nbsp;999` automaticly.
You can configure to not break line:
- after any custom weak word (mostly conjunctions) by language
- inside custom text shortcuts (example: U. S.) by language
- between digits and it's configured units


## Example

Template code:
```php
<p><?php
	// Earth diameter: 6&nbsp;378&nbsp;km. (or&nbsp;6&nbsp;378&nbsp;000&nbsp;m)
	echo $this->LineBreaks(
		'Earth diameter: 6 378 km (or 6 378 000 m).'
	);
?></p>
```
