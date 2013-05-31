# Mediasation Style Guides

The purpose of this guide is to create uniformity among Mediasation code.

The following style guides have been adapted from various industry leaders. When in doubt, refer to their guides.

- [HTML/CSS Style Guide (Google)](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
- [JavaScript (Google)](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)
- [PHP (PHP Framework Interop Group)](http://www.php-fig.org/psr/2)

## 1. General

### Indenting

Code MUST use 4 spaces for indenting, not tabs.

### Lines

Lines should stick to a maximum length of 80 characters; lines exceeding this maximum should be split into multiple subsequent lines of the same maximum length.

No trailing whitespace at the end of non-blank lines.

Blank lines may be added to improve readability and to indicate related blocks of code.

### Naming
- Constants use `ALL_CAPS`
- Variables use `snake_case`
- Functions use `camalCase`
- Classes use `StudlyCaps`
- Private variables and functions are prefixed with an underscore

### Strings
Single-quotes (') are preferred to double-quotes (").

### Control Structures
`if`/`else`/`for`/`while`/`try` always have braces and always go on multiple lines.

	if (condition) {
    	// expressions
	}
 
	while (condition) {
    	// expressions
	}
 
	for (var i = 0; i < 100; i++) {
    	// expressions
	}
 
	if (condition) {
    	// expressions
	} else if (condition) {
    	// expressions
	} else {
    	// expressions
	}
 
	try {
    	// expressions
	} catch (e) {
    	// expressions
	}

### Functions

Function brackets go on a new line aligned with the `function` declaration.

	function someFunction()
	{
	
	}

### Testing for or passing True/False

When testing or passing a boolean, `true` or `false` should be explicitly written out. **Never** use `1` for true or `0` for false.




## 2. HTML

### Capitalization

Use only lowercase
	
	<!-- Recommended -->
	<img src="google.png" alt="Google">
	
### Type Attributes

Omit type attributes for style sheets and scripts. Only use type attributes for style sheets and scripts when **not** using CSS or JavaScript.

Specifying type attributes in these contexts is not necessary as HTML5 implies text/css and text/javascript as defaults. This can be safely done even for older browsers.
	
	<!-- Not recommended -->
	<link rel="stylesheet" href="//www.google.com/css/maia.css" type="text/css">
	<!-- Recommended -->
	<link rel="stylesheet" href="//www.google.com/css/maia.css">
	<!-- Not recommended -->
	<script src="//www.google.com/js/gweb/analytics/autotrack.js" type="text/javascript"></script>
	<!-- Recommended -->
	<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
	
### General Formatting

Use a new line for every block, list, or table element, and indent every such child element.

### HTML Quotation Marks

When quoting attributes values, use double quotation marks.




## 3. CSS

### ID and Class Naming

Use meaningful or generic ID and class names.

Instead of presentational or cryptic names, always use ID and class names that reflect the purpose of the element in question, or that are otherwise generic.

	/* Not recommended: meaningless */
	#yee-1901 {}

	/* Not recommended: presentational */
	.button-green {}
	.clear {}
	
	/* Recommended: specific */
	#gallery {}
	#login {}
	.video {}

	/* Recommended: generic */
	.aux {}
	.alt {}

### ID and Class Name Style

Use ID and class names that are as short as possible but as long as necessary.

	/* Not recommended */
	#navigation {}
	.atr {}
	
	/* Recommended */
	#nav {}
	.author {}
	
### Type Selectors

Avoid qualifying ID and class names with type selectors.

	/* Not recommended */
	ul#example {}
	div.error {}
	
	/* Recommended */
	#example {}
	.error {}
	

### CSS Formatting Rules

- Use only lowercase `color: #e5e5e5;`
- Separate words in ID and class names by a hyphen
- Declarations must be in alphabetical order
- Use a semicolon after the end of every declaration
- Insert a space immediately after the colon following the property name `color: #000;`
- Use single quotation marks instead of double quotation marks
- Use shorthand properties where possible `padding: 0 10px 0 20px;`
- Omit unit specification after "0" values `margin: 0;`
- Omit leading "0"s in values `font-size: .8em`
- Use 3 character hexadecimal notation where possible (`color: #ebc;` instead of `color: #eebbcc;`) 




## 4. JavaScript

### General

Always use semicolons.

### Variables

Variables must **always** be declared with `var`.

Variables declared in succession should be separated by commas and ending with a semicolon following the last declaration.

	var some_variable,
		another_variable,
		yet_another_variable = 'Something';

### Arrays and Objects
Objects and Arrays are declared with shorthand syntax

	var some_array = [],
		some_object = {};



## 5. PHP

### Naming
Follow the general naming guidelines above

Private variables and functions look like the following
  
	private $_some_variable
	
	private _someFunction()
	{
	
	}

### Files

All PHP files must end with a single blank line.

Files should follow the proper MVC pattern of separating application logic and display logic. Exceptions ***may*** be made in cases of MyScripts.

The closing `?>` tag must be omitted from files containing only PHP

### PHP Tags
PHP code must use the long `<?php ?>` tags or the short-echo `<?= ?>` tags; it must not use the other tag variations.

### Keywords and True/False/Null

PHP keywords must be in lower case.

The PHP constants `true`, `false`, and `null` must be in lower case.

### Control Structures

The PHP keyword `elseif` should be used instead of `else if` so that all control
keywords look like single words.

### Classes

Each class must be in a file by itself.

Class brackets go on a new line aligned with the `class` declaration

	class SomeClass
	{
	
	}