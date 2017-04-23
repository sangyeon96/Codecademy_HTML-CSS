# CSS

Unfortunately, the HTML elements that we've used to add content to a web page have resulted in fairly bland results in the browser. For example, it appears that all content seems to be the same color, have the same font, and offer no direct control over the size of the font (apart from the six different heading options). How can we make our HTML more visually appealing?

CSS, or Cascading Style Sheets, is a language that web developers use to **style the HTML content on a web page**. If you're interested in modifying colors, font types, font sizes, shadows, images, element positioning, and more, CSS is the tool for the job!

## `<style>` `</style>` element
`<style>` element allows you to write CSS inside HTML.

```xml
<head>
	<style>

    </style>
</head>
```

But it's better to create `style.css` file. With a CSS file, you can write all the CSS code needed to style a page without having to sacrifice the readability and maintainability of your HTML file.

## `<link>` element
In order to apply the styling to the web page, we'll have to link the HTML file and the CSS file together. The `<link>` element must be placed within the head of the HTML file. It is a self-closing tag and requires the following three attributes:

1. `href` - like the anchor element, the value of this attribute must be **the address, or path, to the CSS file**.
2. `type` - this attribute describes the type of document that you are linking to (in this case, a CSS file). The value of this attribute should be set to `text/css`.
3. `rel` - this attribute describes **the relationship between the HTML file and the CSS file**. Because you are linking to a stylesheet, the value should be set to `stylesheet`.

```xml
<head>
	<link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet">
</head>
```

## CSS Selector
```css
p {

}
```
In the example above, all paragraph elements are selected using a CSS selector.

### Universal Selector
```css
* {
  font-family: Arial;
}
```
In the example above, the universal selector, *, is used to select every element on the page and set the font to Arial.

When all elements on a web page require the same styling, it's often more efficient to set that styling using the universal selector. Afterwards, you can modify (or remove) that styling for specific elements that don't require it.

## CSS declaration
```css
h1 {
	color: Blue;
}
```

To actually style the element, you need to specify two things inside the body of the selector:

1. Property - the property you'd like to style of that element (i.e., size, color, etc.).
2. Value - the value of the property (i.e., 18px for size, Blue for color, etc.).

The line `color: Blue;` is referred to **CSS declaration**. A CSS declaration consists of a **property** and a **value**. Note that a semicolon (;) ends all declarations.

## CSS rule
Finally, the entire snippet of code in the example above is known as a **CSS rule**.
(CSS rule 이미지 삽입)
A CSS rule consists of the **selector** and **all declarations inside of the selector**.

Fortunately, you can select multiple elements at once so that you can save time styling a shared property.
```css
h1, h2, p {
	color: FireBrick;
}
```

## Comments
`/*` `*/`
```css
/* This is a comment in CSS! */
```

## Colors
1. The foreground color
2. The background color

```css
h1 {
	color: MidnightBlue; /* The foreground color */
    background-color: Aqua; /* The background color */
}
```

In CSS, these colors are technically known as **"named colors"**. There are a total of 147 named colors. If you're ever in need of a named color, a quick Google search will yield the results you are looking for.

### RGB colors
RGB (Red, Green, Blue) colors.
RGB colors work by mixing together different amounts of red (R), green (G), and blue (B). Each color (R, G, or B) can take on 1 of a possible 256 values (between 0 and 255). This results in 16,777,216 possible colors.

To use RGB colors, you can use the `rgb()` value when styling a color.
```css
h1 {
  color: rgb(123, 20, 233);
  background-color: rgb(99, 21, 127);
}
```

There are many resources on the Internet known as **"color pickers"** that allow you to view the result of different RGB values before you decide to use a certain color. If you're ever in need of a color picker resource, a quick Google search will yield the results you are looking for.

### Hexadecimal color codes
When specifying an RGB color mixture, the values are in ++base 10++. Hex color codes, however, use ++base 16++, or hexadecimal base (hence the name), to specify color mixtures. All hex color codes begin with a `#` character.
```css
h1 {
  color: #09AA34; /* 09 for R(red), AA for G(green), 34 for B(blue) */
}
```

There are no differences between RGB values and hex color codes. Just different ways to represent color.

### HSL colors
HSL stands for **H**ue, **S**aturation, and **L**ightness. Specifically, this is what each means:

1. Hue - the technical term that describes what we understand as "color." In HSL, hue is represented on a color wheel. It can take on values between 0 and 360.
2. Saturation - the amount of gray in a given color. In HSL, saturation is specified using a percentage between 0% and 100%. The percentage 0% represents a shade of gray, whereas 100% represents full saturation.
3. Lightness - the amount of white in a given color. Similar to saturation, lightness is specified using a percentage between 0% and 100%. The percentage 0% represents black, whereas 100% represents white. 50% is normal.

```css
h1 {
  color: hsl(182, 20%, 50%);
}
```

Note : Because HSL is a part of ++CSS3++, older browsers may not support it.

### Comparing RGB color, Hex color code, HSL color
There is one feature that RGB colors support that hex color codes do not: **opacity**.

Opacity is a measure of how transparent a color is. To modify opacity in RGB colors, CSS offers the `rgba()` value. Note the slight difference in `rgb()` and `rgba()`.

The extra a character in the `rgba()` value is known as the **alpha value**. ++It represents the opacity of a color.++ The alpha value can be a number between 0 or 1, inclusive.

```css
h1 {
  color: rgba(123, 88, 9, 0.5); /* 50% of its normal opacity */
}
```

Note : The alpha value can also be used for HSL colors, using `hsla()`:
```css
h1 {
  color: hsla(239, 45%, 22%, 0.4);
}
```

Older browsers, over time, will become dated (possibly obsolete) and not be able to support newer CSS features. For example, many older browsers do not support RGBa, HSL, or HSLa.

Because of this, we must include redundant color options in our CSS code that can cater to a wide audience of different browsers. Specifically, we can add multiple CSS color declarations, just in case a user's browser can't support a certain declaration.

```css
h1 {
  color: rgb(22, 34, 88);
  color: rgba(22, 34, 88, 0.4);
}
```

Using redundant declarations allow you to support as many users as possible across multiple versions of different Internet browsers.