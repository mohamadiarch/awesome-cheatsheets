# This is a temp for remembering

shell is old. bash is good

:help index

increase terminal pane= ctrl + k or j for switch to another window ==> then ctrl+ up

ctlr + u
ctrl + d
zz
{
}
number+G
? vs / 
I A
f t ,;
gj + gk
--------------
ea
bi
D
d0
dgg
dG
dj + dk
-------------
foo-bquux  # dw:  letters then spaces right of cursor
foo-quux   # daw: letters on both sides of cursor then spaces on the right 
foo- quux  # diw: letters on both sides of cursor
foo-bquux  # dW:  non-whitespace then spaces right of cursor
quux       # daW: non-whitespace on both sides of cursor then spaces on the right
 quux      # diW: non-whitespace on both sides of cursor
--------
surround
vim-expand-region


While j and k typically move down and up one line in Vim, they won't jump between wrapped lines within the same Vim line number. Here are some ways to jump between wrapped lines using j and k with wrap enabled:

1. Using "gj" and "gk":

Prefix j or k with g to move between wrapped lines within the same Vim line number. gj jumps down one wrapped line, while gk jumps up one wrapped line.
2. Using "j/" and "k/" and a search pattern:

You can search for specific terms within the wrapped line to jump directly to that part when using j and k. For example, j/keyword jumps down to the next line containing the word "keyword", while k/another_word jumps up to the previous line containing "another_word".
3. Using dedicated plugins:

Some plugins like vim-jumpline enhance line navigation. With vim-jumpline installed, jJ and kK jump between the first and last lines of the current Vim line, regardless of wrapping.
4. Using visual mode and jL/kL:

Enter visual mode (press v) and select the part of the wrapped line you want to jump to. Then, use jL to jump down and kL to jump up to the beginning of the selected text on the next/previous wrapped line.
Remember, with wrap enabled, Vim considers each wrapped line as part of a larger Vim line number. Using the methods above, you can effectively navigate between these wrapped lines with your preferred j and k shortcuts.

I hope this helps! Feel free to ask if you have any further questions aboutVim and line navigation with wrapping.
