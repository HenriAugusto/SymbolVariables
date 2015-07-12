# Symbol Variables

Is an PureData abstraction that allows you to store symbol as variables and call some methods to work with them.
Here's a non-exhaustive list of what you can do with it with little or no effort:

- Store symbols as variables and call them by their ID.
- Output all your stored symbols, one at a time, on the desired receive.
- Print a list with all your symbols.
- Synchronize your symbols over the internet with other computers. This can be easily done by just using the same
  send name and netsend/netreceive.
- Concatenate Symbols.
- Use multiple instances of Symbol Variables to have separate groups of variables.
- Dynamically search for variable values.

This is in an early stage of development. There's not much methods at the moment but those available are generic enough for you to
achieve more complex things with ease.

#### Methods

Here's a short description of the available methods

- *setvar* -  Initialize a variable and set it's value or change a variable's value.
- *getvar* -  Get a variable value and send it to a desired destination.
- *delete* - Delete a variable.
- *clear* -  Delete all variables.
- *getallvars* -  Send every variable nome to the desired destination, one at a time.
- *getallvalues* -  Send every variable value to the desired destination, one at a time.
- *getallpairs* -  Send every variable nome and value and send them the desired destination, one at a time.
This is a quick combination of the two above, just to make things quicker.
- *printall* - Print every variable and it's name to the console.
- *append/prepend* - Append/Preppend a symbol to one variable's value.
- *appendall/prependall* - Append/Preppend a symbol to all variable's value.
- *concatenate* - Concatenate a list of symbols and store the result in a variable.
- *concatenateall* - Concatenate every variable and store the result in a variable.
- *frequency* - Returns the number of variables that has a specific value.
- *copy* -Copy the variableslist to a message box.
- *set* - Set the entire variable list.
- *varindex* - Returns the index of a variable on the master list.
- *search* - Returns the index of every variable that contains a specific value.
- *getbyindex* - Returns the variable name or value on the specified index of the master list.
- *compare* - Compare a list of symbols and returns true if they're all equal.

##### Dependencies

_Symbol Variables_ uses the [EasyFlow](https://github.com/HenriAugusto/EasyFlow.git) library.
