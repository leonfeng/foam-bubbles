# Useful JavaScript Snippets

## Complete an entire section in a Udemy course

```javascript
const section = document.querySelector('div[data-purpose="section-panel-16"]');
const checkboxes = section.querySelectorAll(
	'input[type="checkbox"]:not(:checked)'
);
for (let cb of checkboxes) {
	cb.click();
}
```

## Clear Twitter interests

```javascript
const intervalID = setInterval(() => {
	const cb = document.querySelector('input[type="checkbox"]:checked');
	if (!cb) {
		clearInterval(intervalID);
		return;
	}
	cb?.click();
}, 500);
```

## Clear Twitter topic suggestions

```javascript
const intervalID = setInterval(() => {
	const btn = document.querySelector('div[aria-label*="Dismiss"]');
	if (!btn) {
		clearInterval(intervalID);
		return;
	}
	btn?.click();
}, 500);
```
