# HTML & CSS Essentials Practice

This project is a practical guide and hands-on exploration of fundamental HTML and CSS concepts. It’s designed to help learners understand the layout behavior of web elements, CSS styling rules, and responsive design techniques.

## The CSS Box Model

The CSS Box Model is at the core of web layout. Each HTML element is treated as a box, comprising four layers:

1. **Content**: This is where text, images, or other elements live. Controlled by `width` and `height`.
2. **Padding**: Clears an area around the content, inside the border.
3. **Border**: Encapsulates the padding and content, and can be styled.
4. **Margin**: Provides space between the element and its neighbors.

###  Total Element Size

To compute the complete dimensions of an element:

```
Total Width = content + left/right padding + left/right border + left/right margin
Total Height = content + top/bottom padding + top/bottom border + top/bottom margin
```

> **Tip:** Use `box-sizing: border-box` to make width and height include padding and border.

##  Block vs Inline Elements

### Block-Level Elements

- Start on a new line.
- Take full width available.
- Can contain both inline and block elements.

**Examples:**  
`<div>`, `<p>`, `<section>`, `<ul>`, `<li>`, `<header>`, `<footer>`

### Inline Elements

- Do not start on a new line.
- Occupy only the space their content needs.
- Usually used within block elements.

**Examples:**  
`<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<code>`

### Overriding Defaults

```css
div {
    display: inline;
}

span {
    display: block;
}
```

##  CSS Positioning

Positioning controls how an element is placed on the page:

- **relative**  
    Offset from its normal position.  
    Still occupies original layout space.

    ```css
    .element {
        position: relative;
        top: 10px;
        left: 15px;
    }
    ```

- **absolute**  
    Positioned relative to the nearest positioned ancestor.  
    Removed from document flow.

    ```css
    .container {
        position: relative;
    }

    .child {
        position: absolute;
        top: 0;
        left: 0;
    }
    ```

##  Utility & Reusable Classes

Commonly used classes in modern CSS workflows:

- **Structure:** `.container`, `.row`, `.col`, `.section`, `.header`, `.footer`, `.card`
- **Spacing:** `.m-1`, `.p-2`, `.m-auto`, `.p-0`, `.m-0`
- **Text & Visibility:** `.text-center`, `.text-left`, `.hidden`, `.visible`
- **Buttons & Borders:** `.btn`, `.btn-primary`, `.border`, `.rounded`, `.shadow`

##  CSS Specificity

CSS decides which rules to apply based on specificity:

- **Inline styles:** (1, 0, 0, 0)
- **IDs:** (0, 1, 0, 0)
- **Classes, attributes, pseudo-classes:** (0, 0, 1, 0)
- **Elements, pseudo-elements:** (0, 0, 0, 1)
- **Universal selector:** (0, 0, 0, 0)

The more specific the selector, the higher the priority.

| Selector   | Specificity   |
|------------|--------------|
| `#header`  | (0,1,0,0)    |
| `.nav-item`| (0,0,1,0)    |
| `div p`    | (0,0,0,2)    |
| `style=""` | (1,0,0,0)    |

##  Responsive Design with Media Queries

Adapt layouts for different screen sizes using breakpoints:

```css
@media (max-width: 600px) {
    /* Mobile phones */
}

@media (min-width: 601px) and (max-width: 1024px) {
    /* Tablets */
}

@media (min-width: 1025px) {
    /* Desktops */
}
```

##  Flexbox & Grid

**Flexbox (1D layout)**  
Use for linear arrangements.

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

**Grid (2D layout)**  
Ideal for complex page layouts.

```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
}
```

##  Essential Meta Tags

These tags live inside `<head>` and control rendering, SEO, and layout.

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="description" content="Practice HTML & CSS fundamentals.">
<meta name="author" content="Your Name">
```

##  Getting Started

No setup needed. Just open `index.html` in your browser and inspect the layout, styles, and structure.

##  Project Structure

```
practice-html/
├── index.html
├── style.css
├── /assets
│   └── images, icons, etc.
```
