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

## Open last file
Press `Ctrl + o + o`. Vim will open the last file and it will even keep the
cursor position.

## Vi in the command line
For using vi capabilities in the command line, type

```
set -o vi
```

Then you can enter tu vi mode by pressing ESC

> Just allows the one line editting features

[source](https://dalibornasevic.com/posts/43-12-vim-tips)

# Useful resources
* [12 Vim Tips](https://dalibornasevic.com/posts/43-12-vim-tips)
* [Learn Vim Progressively](http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)
