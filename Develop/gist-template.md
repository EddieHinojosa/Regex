# Regex Tutorial for HEX values

Regex (Regular expressions) can help a tool used to match what youbare searching via text.
below will hvae a breakdown of how Hexadecimal values can be matched to finds the color you are looking for, including minimizing errors regarding cap sensitive input.

## Summary

<p>The purpose of Hexadecimal(HEX) values is to pull a percise color located on the color wheel/block.
<p>Hex values can be search in various degrees of filters, it can be search from: <br>
3-digit shorthand (e.g., #FFF) <br>
6-digit full (e.g., #FFFFFF) <br>
4-digit with alpha (e.g., #FFF7) <br>
8-digit with alpha (e.g., #FFFFFFFF) <br>
</p>


<p>the code below will search based on the input given to locate the color desired.</p>

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

to make the search `case insensitive` you'll have to add `i` at the end: <br>
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/i`

alternatively you can also include upper case charaters: <br>
`/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`


## Author

created by EddieHinojosa @ [https://github.com/EddieHinojosa](https://github.com/EddieHinojosa)
