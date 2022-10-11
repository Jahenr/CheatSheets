# Javascript Cheatsheet

# Object Properties

## Object Length
length is a property of a function object, and indicates how many arguments the function expects, i.e. the number of formal parameters. This number does not include the rest parameter. Has a value of 1.
```
Object.length
```

## Object Prototype
Represents the Object prototype object and allows to add new properties and methods to all objects of type Object.
```
Object.prototype 
```

# Object Constructor Methods

## Object assign
Copies the values of all enumerable own properties from one or more source objects to a target object. method is used to copy the values of all enumerable own properties from one or more source objects to a target object. It will return the target object
```
Object.assign(target, ...sources)
```

## Object Create
Creates a new object with the specified prototype object and properties. The object which should be the prototype of the newly-created object.
```
Object.create(MyObject)
```

## Object Property Define
Adds the named property described by a given descriptor to an object.
```
Object.defineProperty(obj, prop, descriptor)
```
OR

Adds the named properties described by the given descriptors to an object.
```
Object.defineProperties(obj, props)
```

## key return
Returns an array containing all of the [key, value] pairs of a given object's own enumerable string properties.
```
Object.entries(obj)
```

## object freeze
Freezes an object: other code can't delete or change any properties.
```
Object.freeze(obj)                                 
```

## Property Descriptor
Returns a property descriptor for a named property on an object.
```
Object.getOwnPropertyDescriptor(obj, prop)           
```
OR
Returns an object containing all own property descriptors for an object.
```
Object.getOwnPropertyDescriptors(obj)                
```

### Only names
Returns an array containing the names of all of the given object's own enumerable and non-enumerable properties.
```
Object.getOwnPropertyNames(obj)                      
```

### Only symbols
Returns an array of all symbol properties found directly upon a given object.
```
Object.getOwnPropertySymbols(obj)                    
```

## prototype descriptor
Returns the prototype of the specified object.
```
Object.getPrototypeOf(obj)                           
```

## Comparator
Compares if two values are the same value. Equates all NaN values (which differs from both Abstract Equality Comparison and Strict Equality Comparison).
```
Object.is(value1, value2);                           
```

## extensibility check
Determines if extending of an object is allowed.
```
Object.isExtensible(obj)                             
```

## Freeze Check
Determines if an object was frozen.
```
Object.isFrozen(obj)                                 
```

## Seal Chcek
Determines if an object is sealed.
```
Object.isSealed(obj)                                 
```

## key value
Returns an array containing the names of all of the given object's own enumerable string properties.
```
Object.keys(obj)                                     
```

## Extension lock
Prevents any extensions of an object.
```
Object.preventExtensions(obj)                        
``` 
## Object Seal
Prevents other code from deleting properties of an object.
```
Object.seal(obj)                                     
``` 

## prototype property set
Sets the prototype (i.e., the internal [[Prototype]] property).
```
Object.setPrototypeOf(obj, prototype)                
```

## Object value 
Returns an array containing the values that correspond to all of a given object's own enumerable string properties.
```
Object.values(obj)                                   
```

## Object property
Object instances and Object prototype object 
```
Object.prototype.property 
```
or 
```
Object.prototype.method()
```
or
```
obj.constructor                                      
```
or 
```
obj.__proto__                                        
```

# Methods

## property
Returns a boolean indicating whether an object contains the specified property as a direct property of that object and not inherited through the prototype chain.
```
obj.hasOwnProperty(prop)                             
```

## Prototype chain check
Returns a boolean indicating whether the object this method is called upon is in the prototype chain of the specified object.
```
prototypeObj.isPrototypeOf(object)                   
```

## Enumerability Check
Returns a boolean indicating if the internal ECMAScript [[Enumerable]] attribute is set.
```
obj.propertyIsEnumerable(prop)                       
```

## Find string
Calls toString().
```
obj.toLocaleString()                                 
```

## String Return
Returns a string representation of the object.
```
obj.toString()                                       
```

## object value
Returns the primitive value of the specified object.
```
object.valueOf()                                     
```

# GLOBAL OBJECTS > ARRAY

# properties
## Array Length
Reflects the number of elements in an array.
```
Array.length                                         
```

## array prototype
Represents the prototype for the Array constructor and allows to add new properties and methods to all Array objects.
```
Array.prototype                                      
``` 

# Array methods

## range
Creates a new Array instance from an array-like or iterable object.
```
Array.from(arrayLike[, mapFn[, thisArg]])            
```

## Array Check
Returns true if a variable is an array, if not false.
```
Array.isArray(obj)                                   
```

## Reconstruction
Creates a new Array instance with a variable number of arguments, regardless of number or type of the arguments.
```
Array.of(element0[, element1[, ...[, elementN]]])    
```

# mutator methods

## Copy
Copies a sequence of array elements within the array.
```
arr.copyWithin(target, start, end)                   
```

## Fill
Fills all the elements of an array from a start index to an end index with a static value. 
```
arr.fill(value, start, end)                          
``` 

## pop
Removes the last element from an array and returns that element. 
```
arr.pop()                                            
``` 

## flat
merges nested array into one single array 
```
arr.flat()                                           
``` 

## push
Adds one or more elements to the end of an array and returns the new length of the array. 
```
arr.push([element1[, ...[, elementN]]])              
``` 

## reverse
Reverses the order of the elements of an array in place — the first becomes the last, and the last becomes the first. 
```
arr.reverse()                                        
``` 

## shift by 1
Removes the first element from an array and returns that element. 
```
arr.shift()                                          
``` 

## sorting
Sorts the elements of an array in place and returns the array. 
```
arr.sort()                                           
``` 

## slicing
Adds and/or removes elements from an array. 
```
array.splice(start, deleteCount, item1, item2, ...)  
``` 

## unshift
Adds one or more elements to the front of an array and returns the new length of the array. 
```
arr.unshift([element1[, ...[, elementN]]])           
``` 

# accessor methods

## concatenation
Returns a new array comprised of this array joined with other array(s) and/or value(s). 
```
arr.concat(value1[, value2[, ...[, valueN]]])        
``` 

## search check
Determines whether an array contains a certain element, returning true or false as appropriate. 
```
arr.includes(searchElement, fromIndex)               
``` 

## search by index
Returns the first (least) index of an element within the array equal to the specified value, or -1 if none is found. 
```
arr.indexOf(searchElement[, fromIndex])              
``` 

## joiner
Joins all elements of an array into a string. 
```
arr.join(separator)                                  
``` 

## search index last
Returns the last (greatest) index of an element within the array equal to the specified value, or -1 if none is found. 
```
arr.lastIndexOf(searchElement, fromIndex)            
``` 

## slicing
Extracts a section of an array and returns a new array. 
```
arr.slice(begin, end)                                
``` 

## typecast to string
Returns a string representing the array and its elements. Overrides the Object.prototype.toString() method. 
```
arr.toString()                                       
``` 

## localize string
Returns a localized string representing the array and its elements. Overrides the Object.prototype.toLocaleString() method. 
```
arr.toLocaleString(locales, options)                 
``` 

# iteration methods
## new array creation
Returns a new Array Iterator object that contains the key/value pairs for each index in the array. 
```
arr.entries()                                        
``` 

## array test on each element
Returns true if every element in this array satisfies the provided testing function. 
```
arr.every(callback[, thisArg])                       
``` 

## filter
Creates a new array with all of the elements of this array for which the provided filtering function returns true. 
```
arr.filter(callback[, thisArg])                      
``` 

## find/locate
Returns the found value in the array, if an element in the array satisfies the provided testing function or undefined if not found. 
```
arr.find(callback[, thisArg])                        
``` 

## find id
Returns the found index in the array, if an element in the array satisfies the provided testing function or -1 if not found. 
```
arr.findIndex(callback[, thisArg])                   
``` 

## call on condition loop
Calls a function for each element in the array. 
```
arr.forEach(callback[, thisArg])                     
``` 

## array key value
Returns a new Array Iterator that contains the keys for each index in the array. 
```
arr.keys()                                           
``` 

## map
Creates a new array with the results of calling a provided function on every element in this array. 
```
arr.map(callback[, initialValue])                    
``` 

## reduction
Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value. 
```
arr.reduce(callback[, initialValue])                 
``` 

## right reduction
Apply a function against an accumulator and each value of the array (from right-to-left) as to reduce it to a single value. 
```
arr.reduceRight(callback[, initialValue])            
``` 

## OR type test
Returns true if at least one element in this array satisfies the provided testing function. 
```
arr.some(callback[, initialValue])                   
``` 

## return value by id
Returns a new Array Iterator object that contains the values for each index in the array. 
```
arr.values()                                         
```