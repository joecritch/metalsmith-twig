metalsmith-twig [![Build Status](https://travis-ci.org/PKuebler/metalsmith-twig.svg?branch=master)](https://travis-ci.org/PKuebler/metalsmith-twig)
===========

## A [metalsmith](http://www.metalsmith.io/) Plugin for [Twig](http://twig.sensiolabs.org/) based on [justjohn/twig.js](https://github.com/justjohn/twig.js).

# Install

```bash
  npm install metalsmith-twig
```

Configuration in `metalsmith.json`:

	{
	  "plugins": {
	    "metalsmith-twig": {}
	  }
	}

# Examples

## Initialize (INIT):

```js
var Metalsmith = require('metalsmith'),
	Twig = require('metalsmith-twig');

Metalsmith(__dirname)
	.use(twig())
	.build(function(err) {
		if (err) throw err;
	});
```

### Options:

* `directory`: *(default: views)* the directory for views.
* `global`: *(default: {})* global variables.

## Files

Source file src/index.md:

```markdown
---
layout: layout.html
title: The title
---
The Content
```

## View

View `views/layout.html`:

```html
<!doctype html>
<html>
	<head>
		<title>{{title}}</title>
	</head>
	<body>
		{{contents}}
	</body>
</html>
```

# Docs

* Twig.js [github.com/justjohn/twig.js](https://github.com/justjohn/twig.js)
* Twig [twig.sensiolabs.org](http://twig.sensiolabs.org/)

# The MIT License (MIT)