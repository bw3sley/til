# Shorthand properties
**Shorthand properties** are CSS properties that let you set the values of multiple other CSS properties simultaneously. Using a shorthand property, you can write more concise (and often more readable) style sheets, saving time and energy.

</br>

## Background properties
A background with the following properties ...

```css
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;
```

... can be shortened to just one declaration:

```css
    background: #000 url(images/bg.gif) no-repeat left top;
```

## Font properties
The following declarations ...

```css
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;
```

... can be shortened to the following:

```css
    font: italic bold .8em/1.2 Arial, sans-serif;
```

## Border properties
With borders, the width, color, and style can be simplified into one declaration. For example, the following CSS ...

```css
    border-width: 1px;
    border-style: solid;
    border-color: #000;
```

... can be simplified as:

```css
    border: 1px solid #000;
```

## Margin and padding properties
Shorthand versions of margin and padding values work similarly; the margin property allows for shorthand values to be specified using one, two, three, or four values. The following CSS declarations ...

```css
    margin-top: 10px;
    margin-right: 5px;
    margin-bottom: 10px;
    margin-left: 5px;
```

... are the same as the following declaration using the four value shorthand. Note that the values are in clockwise order, beginning at the top: top, right, bottom, then left (TRBL, the consonants in "trouble").

```css
    margin: 10px 5px 10px 5px;
```

Margin shorthand rules for one, two, three and four value declarations are:

- When **one** value is specified, it applies the same margin to all four sides.
- When **two** values are specified, the first margin applies to the top and bottom, the second to the left and right.
- When **three** values are specified, the first margin applies to the top, the second to the left and right, the third to the bottom.
- When **four** values are specified, the margins apply to the top, right, bottom, and left in that order (clockwise).

For more shorthands: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)