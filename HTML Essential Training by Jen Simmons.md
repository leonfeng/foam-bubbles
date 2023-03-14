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

```html
<p lang="fr">
	Jeremy Keith a dit:
	<q>Vous pouvez ouvrir un document HTML de l'époque dans un navigateur
		aujourd'hui.</q>
</p>
```

```html
<p lang="bg">
	Джереми Кийт каза,
	<q>че днес можете да отворите HTML документ от тогава в браузъра.</q>
</p>
```
