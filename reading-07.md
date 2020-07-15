# Collections

## Collections
- A collections is a type of data that can key value references, but it is of variable length so it has more flexibility than an array.
- Example declaration: ```var salmons = new List<string>();``` or ```var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };```.
- These collections can be looped through using ```for``` and ```foreach``` statements.
- Unless otherwise specified, collections have behaviors very similar to arrays. If the collection is instantiated with key/value pairs, then it add another way to access values.
- Key/Value pair declarations: ```Dictionary<string, Element> elements = BuildDictionary();```.
- LINQ queries can be used to access items in a collection. LINQs return new collections that contain only the desired items.
- Collections can be sorted using ```.Sort()```; may require use of ```IComparable<T>``` and/or ```CompareTo()``` method.
- Iterators can be used for looping through Collections.
- Custom Collections can be declared, but need addition methods and classes to make them function.

## Enums
- Enums are value types that are defined by a set of named constants of the underlying numeric integral type.
- By default, the numeric integral type is ```int```, starting at 0 and increasing by one for each definition in order, but custom integrals value types can be set upon declaration.
- Enums can be used as bit flags so that bitwise operators can be applied to them. By using powers of two (easy in binary) it removes any ambiguity for combinations of enums, since no two combinations can equal the combination of any other two flags.
- To access an enum's integral numeric, cast it when referencing it: ```(enumName)1```.



[Table of Contents](README.md)