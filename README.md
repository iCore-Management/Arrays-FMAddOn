[iCore Management](https://icoremanagement.com)

# Arrays -AddOn

Arrays is a suite of 30+ custom functions that bring javascript array methods to FileMaker using native functionality without external dependencies.

## Contents

| Function | Discription |
| --- | --- |
| ~array | Return the current value of ~array |
| ~array.concat( array ) | Joins an array to the end of ~array, and returns a copy of the joined arrays. Does not change ~array |
| ~array.copyWithin( target ; start ; end ) | Copies ~array elements within the array, to and from specified positions  |
| ~array.entries | Returns a key/value pair list from ~array |
| ~array.every( function ) | Checks if every element in ~array passes a test |
| ~array.fill( value ; start ; end ) | Fill the elements in a ~array with a static value |
| ~array.filter( function ) | Creates a new array with every element from ~array that passes a test |
| ~array.find( function ) | Returns the first element from ~array that passes a test |
| ~array.findIndex( function ) | Returns the index of the first element from ~array that passes a test |
| ~array.forEach( function ) | Calls a function for each ~array element. Does not change ~array |
| ~array.from( values ) | Creates ~array from a list. Sets ~array |
| ~array.includes( value ) | Check if ~array contains the specified element |
| ~array.indexOf( value ; start ) | Search ~array for an element and return its position |
| ~array.isArray( array ) | Checks whether array is an array |
| ~array.join( seperator ) | Joins all elements of ~array into a string |
| ~array.keys | Returns a list containing the keys of the ~array |
| ~array.lastIndexOf( value ; start ) | Search ~array for an element, starting at the end, and return its index |
| ~array.map( function ) | Creates a new array with the result of calling a function for each ~array element |
| ~array.pop | Removes the last element of ~array, and returns that element |
| ~array.push( values ) | Adds new elements to the end of ~array, and returns the new length |
| ~array.reduce( function ; initialValue ) | Reduce the values of ~array to a single value (going left-to-right) |
| ~array.reduceRight( function ; initialValue ) | Reduce the values of ~array to a single value (going right-to-left) |
| ~array.reverse | Reverses the order of the elements in ~array. Changes ~array |
| ~array.shift | Removes the first element of ~array, and returns that element. Changes ~array |
| ~array.slice( start ; end ) | Selects a part of ~array, and returns the new array. Does not change ~array |
| ~array.some( function ) | Checks if every element in ~array passes a test |
| ~array.sort( function ) | Sorts the elements of ~array |
| ~array.splice( index ; remove ; values ) | Adds/Removes elements from ~array |
| ~array.toString | Converts an array to a string, and returns the result as a comma seperated list |
| ~array.unshift( value ) | Adds new elements to the beginning of ~array, and returns the new length |
| ~array.valueOf( array ) | Returns the primitive value of an array. Sets ~array |
| ~array.length( array ) | Return the length of array |

## Installation

Once the Add-On is dragged onto the layout, the custom functions will be added for use.

## Usage

These functions work by setting and manipulating a local variable, $~array.  $~array can be set by calling ~array.valueOf ( array ), and passing the array value to set, or calling ~array.from ( values ) and passing a list of values.  Once set, $~array can be returned by using the getter function, ~array.

To send a function as a parameter, the function must be quoted text. The text function will then be evaulated inside the ~array function. A number of internal variuables can be used within the quoted function and are substituted in before evaulation.

			[value]		replaced with array value during run time
			[index]		replaced with array index during run time
			[array]		replaced with array during run time
			[total]		replaced with result value during run time

