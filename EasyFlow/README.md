# EasyFlow

_EasyFlow_ is an library of PureData abstractions oriented at simplifying your work by resuming frequent parts of the data flow.
For example you can store a list on _PickList_ by sending it to it's cold inlet and, by sending numbers to it's hot inlet get
it's element. Or you can have a _Counter object_ instead of having to type [float] [+ 1] etc every time. Even better: there is a
_For_ object that is a [until] with an integrated counter.


Lots of EasyFlow abstractions uses other abstractions from the library. In those cases, that other abstractions were included
as subpatches to eliminate dependencies. This way you can simply copy the abstractions you need.

##### Abstractions

- *Alternate* - Passes it's input one time to the left, then to the right, then to the left...
- *Counter* - Simple counter object. Hot inlet raises it. Cold inlet sets it.
- *concatenate* - Concatenate a list of symbols that it receives.
- *CopyList* - Copies a list on a message box.
- *For* - Works like until, but with an integrated counter on it's right outlet. It "bangs" on it's left outlet.
- *L2R* - (Left to Right) - Takes a list and outputs it's elements one at a time, from left to right order.
- *R2L* - (Right to Left) - Takes a list and outputs it's elements one at a time, from right to left order.
- *Funnel* - Abstraction that switches between l2r and r2l.
- *GetNthElement* - Receives an index N on it's cold inlet and when it receives a list on it's hot inlet,
it outputs it's Nth element. Similar is _ListPick_ - see below
- *GetPair* - Works like GetNthElement, but takes the Nth element and it's sucessor.
- *ListPick* - Store a list on it's cold inlet and get it's elements by sending it's indexes on ListPick
hot inlet. Works with the inverse order of GetNthElement. Notice what triggers the output on each abstraction.
- *ListStore* - Stores a list just like a [float] stores a float. I'm seriously thing about renaming it
to "FranzList"
- *PopNthElement* - Passes a list through without it's N-th element.
- *Search* - Search for a specific value on a list and outputs it's indexes. Outputs -1 if not found.
- *SearchNDestroy* - Store symbols as variables and call them by their ID.
- *SubstituteNthElement* - Passes a list through without it's N-th element.
- *Switch* - Passes it's input through it's left or right outlet depending on what you send to it's cold inlet.
- *Symbolize* - Gets a word in a message box and makes it into a symbol.
