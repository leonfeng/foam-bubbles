# HTML Essential Training by Jen Simmons

## Headlines

There isn't a strict formula. You just want to use the six levels of options to create semantic hierarchy in your use of headlines.

## Bold and italics

### Italics

`<i>` - visual only italics

`<em>` - emphasis italics

Example

```html
My <em>favorite</em> character from <i>Sesame Street</i> is Grover.
```

### Bold

`<strong>` - importance, seriousness, urgency

`<b>` - bold

Examples

```html
<h1><strong>Warning!</strong> Do not be late.</h1>
```

```html
<h2><strong>Chocolate and coffee</strong> and other things I crave</h2>
```

```html
<p>
	…, and <b>we want to mark certain phrases with some boldness</b>, some
	visual attention, …
</p>
```

## Lists

### Unordered lists

Used for lists, nav menus, article cards, etc.

### Ordered lists

### Definition lists

Key-value pairs

```html
<dl>
	<dt>term</dt>
	<dd>definition</dd>
	<dd>additional definition</dd>
	<dt>second term</dt>
	<dd>definition of second term</dd>
	<dt>third term</dt>
	<dd>definition of third term</dd>
</dl>
```

## Quotes

### Blockquotes

```html
<blockquote>
	<p>Lorem ipsum</p>
	<cite>—Jane Doe</cite>
</blockquote>
```

### Inline Quotes

Different quotation marks depending on locale.

```html
<p>
	Jeremy Keith said,
	<q>You could open an HTML document from back then in a browser today.</q>
</p>
```

<!-- prettier-ignore-start -->
```html
<p lang="fr">
	Jeremy Keith a dit:
	<q>Vous pouvez ouvrir un document HTML de l'époque dans un navigateur aujourd'hui.</q>
</p>
```
<!-- prettier-ignore-end -->

```html
<p lang="bg">
	Джереми Кийт каза,
	<q>че днес можете да отворите HTML документ от тогава в браузъра.</q>
</p>
```

## Dates and times

```html
<time datetime="2025-05-08">May 8, 2025</time>
```

```html
<time>on the 8th of May next year</time>
```

```html
<time datetime="15:45-05:00">3:45pm in New York</time>
```

```html
<time datetime="2020-11-04T19:00">Wednesday, Nov 4th at 7p</time>
```

## Code, pre, and br

### `<code>`

```html
<p>
	We can write <code>{color:green;}</code> in our CSS, and it will apply to
	anything marked up as an <code>&lt;H4&gt;</code> element.
</p>
```

### `<pre>`

```html
<h1>[in Just-]</h1>
<p>by e.e. cummings</p>
<pre>
it's
spring
and

        the

                goat-footed

balloonMan        whistles
far
and
wee
</pre>
```

![](attachments/Screenshot%202021-05-24%20133207.png)

## Superscripts, subscripts, and small text

### `<sub>`

```html
<p>H<sub>2</sub>O</p>
```

### `<sup>`

```html
<p>Something that has a footnote.<sup>2</sup></p>
```

### `<small>`

To convey something that has very little prominence

```html
<small>&copy; 2019 Fancy Company</small>
```

## HTML attributes

### Global Attributes

Work on any HTML element.

`class`, `id`

`contenteditable`

`lang`, `dir`
