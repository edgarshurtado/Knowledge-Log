# VIM NOTES

## Switching case of characters
* Toggle case "HellO" to "hELLo" with `g~` then a movement.
* Uppercase "HellO" to "HELLO" with `gU` then a movement.
* Lowercase "HellO" to "hello" with `gu` then a movement.

## Use of registers
You can use peronalized buffers to copy text in vim. i.e. "ayw.
This will yank the current word and store it at the "a register
> The use of the " is mandatory

If insted a lowercase letter you use a capital letter  (i.e. "A), 
whatever you copy will be add to what you had previously on the 
register with lowercase letter

The system clipboard is at the "+ register. It can be use for copy
and for pasting
