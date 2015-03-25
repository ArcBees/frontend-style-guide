# HTML Structure and Rules

## Syntax

- Soft tabs, 4 spaces
- Nested elements should be indented
- Only use lowercase on HTML element names, attributes and values (except for text)
- Don't add value on boolean attribute (_disabled_, _selected_, _checked_ ...) : `<input type="text" disabled>`
- Paragraphs of text should always be placed in a `<p>` tag. Never use multiple `<br>` tags

## Page

- HTML5 doctype `<!DOCTYPE html>`
- Default language attribute specified `<html lang="en-us">`
- Character encoding specified `<meta charset="utf-8">`
- Each page should have its own `<title>`
- If the page has to be referenced, include a custom `<meta name="description">` and required SEO tags (like _og_ tags)

## JS hooks

It is not a good idead to bind your CSS and your JS onto the same class. By doing so means you can't have (or remove) one without (removing) the other. It is much cleaner, much more transparent, and much more maintainable to bind your JS onto specific classes.

Prefix these classes with `js-` : `<a class="js-toggler">`
