# Style Guide - v0.2 

### Last updated: 05/31/2013 at 4:15pm


## New in version 0.2

### Files

Lines **must** use the Unix LF (linefeed) line ending.

#### File Names

- MyScripts, CSS, JavaScript, and PHP view files should be lowercase and use hyphens to separate words: `some-awesome-file.js`
- PHP Class file names should match their class names: `TheClassName.php`

### Documentation

Documents should include descriptive comments in the form of DocBlocks. DocBlock syntax is similar across languages, but may vary from language to language.

PHP files should use [phpDocumentor](http://www.phpdoc.org/) for syntax reference and documentation generation.

JavaScript files should use [YUIDoc](http://yui.github.io/yuidoc/) for syntax reference and documentation generation.

### Alignment & Spacing

Arrays and Objects with more than **one** item must break each item onto a new line indented once

	$person = array(
		'first_name' => 'John',
		'last_name' => 'Doe'
	);




## Updated in version 0.2

### Naming

- PHP Classes and JavaScript Object Classes use `StudlyCaps`

### Strings

String concatenation **must** have a space before and after each concatenating operator.

	// PHP
	$new_string = 'Johnny ran ' . $distance . ' miles on ' . $day . ' morning.';
	
	// Javascript
	var new_string = 'Johnny ran ' + distance + ' miles on ' + day + ' morning.';
	
### CSS Formatting Rules

- Use a semicolon after the end of every declaration *except* the last declaration in a block 

## PHP

### Files

Files containing only PHP must end with a single blank line.

### Strings

Manually concatenate strings and variables. 

	// not recommended
	$some_var = "Good morning $name.";
	
	// recommended
	$some_var = 'Good morning ' . $name . '.';