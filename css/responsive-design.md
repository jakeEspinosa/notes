# Responsive Design
## Media Queries
You can do them through HTML, JS, and CSS, not just CSS. CSS is the best practice tho
Use flexbox and media queries to do breakpoints (media queries will change the flex-direction).
```css
@media screen (min-wdith: 320px) and (max-width: 768px)
```
### Viewport Meta Tag
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
This makes the webpage's width match the device's width and sets the initial zoom level.
Necessary to make media queries work
## Best Practices
Usually, if you are assigning `width` to a flex item, you are better off using grid.
Use `clamp` for responsive text.
