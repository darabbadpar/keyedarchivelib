# keyedarchivelib

TODO: Support python3.7

Basic Python (>=3.8) library to generate and parse NSKeyedArchive files.

## Installation

**Python 3.8 or above** is required due to a requirement on the `plistlib.UID` standard library class and associated functionality.

Install with pip:

``pip3 install keyedarchivelib``

## Usage

The `keyedarchivelib` module has the same interface as the `plistlib` standard library module:

`load`, `loads`, `dump`, and `dumps` have the same function signatures as [plistlib](https://docs.python.org/3/library/plistlib.html).

The `keyedarchivelib` module includes type hints.

For convenience, examples are provided below: 

### Reading (`load` & `loads`)

````python
from keyedarchivelib import load

with open("example.plist", 'rb') as fp:
    pl = load(fp)
print(pl["test"])
````

### Writing (`dump` & `dumps`)

````python
from keyedarchivelib import dump, dumps

example_dict = {
    "test": 1 
}
with open("example.plist", 'wb') as fp:
    dump(example_dict, fp)

# ~~~ OR ~~~

print(dumps(example_dict))
````
