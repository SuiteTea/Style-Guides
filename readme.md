# Style Guide - v1.0

### Last updated: 02/19/2014 at 11:15am


## Updated in version 1.0

### Naming

- Private javascript variables and methods ***may*** be prefixed with a single underscore to indicate visibility.
- Private PHP variables and methods ***must not*** be prefixed with an underscore to indicate visibility.
- Global/helper functions use `snake_case`.

## CSS

### Formatting

Declarations ***should*** be in alphabetical order.


## PHP

### Strings

Strings and variables ***should*** be manually concatenated. 

	// not recommended
	$some_var = "Good morning $name.";
	
	// recommended
	$some_var = 'Good morning ' . $name . '.';
	
### Classes

Class brackets immediately follow a single space after the class declaration on the same line

	class SomeClass {
	
	}