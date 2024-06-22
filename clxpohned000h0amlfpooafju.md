---
title: "Mastering DOM Manipulation in JavaScript: Essential Techniques"
datePublished: Sat Jun 22 2024 05:27:31 GMT+0000 (Coordinated Universal Time)
cuid: clxpohned000h0amlfpooafju
slug: mastering-dom-manipulation-in-javascript-essential-techniques
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/g5jpH62pwes/upload/96aff3ffc109f246830f9e31f49e2510.jpeg
tags: javascript, dom, essential, dom-manipulation

---

Web development often involves manipulating the Document Object Model (DOM) to create dynamic, interactive web pages. Becoming proficient in DOM manipulation is crucial for any developer. This guide will cover 14 essential techniques that will make you a DOM manipulation master.

Welcome back to Web Dev Simplified! I'm Kyle, and my goal is to simplify web development so you can build your dream projects faster.

If you're eager to elevate your JavaScript skills, consider subscribing to my channel for more tutorials. For a more comprehensive learning experience, check out my full JavaScript course linked in the description below.

## Adding Elements to the Page

### Using `append` and `appendChild`

Adding elements to your webpage is foundational. You can add elements using two methods: `append` and `appendChild`. Here's how to do it:

1. **Select the Element**:
    
    ```javascript
    const body = document.body;
    ```
    
2. **Appending Strings and Elements**:
    
    * With `append`:
        
        ```javascript
        body.append('Hello World');
        ```
        
    * With `appendChild`:
        
        ```javascript
        const div = document.createElement('div');
        body.appendChild(div);
        div.innerText = 'Hello World';
        ```
        
    
    While `appendChild` only accepts nodes, `append` can handle strings and multiple elements at once, making it more versatile.
    

### Creating Elements

To create a new element, use `document.createElement`:

```javascript
const div = document.createElement('div');
body.append(div);
```

## Modifying Text Inside Elements

### Using `innerText` and `textContent`

You can modify the text inside elements using `innerText` or `textContent`:

```javascript
div.innerText = 'Hello World';
div.textContent = 'Hello World 2';
```

* `innerText` considers the CSS and only includes visible text.
    
* `textContent` includes all text, even if it's not visible due to CSS.
    

## Modifying HTML Inside Elements

Use `innerHTML` to insert HTML:

```javascript
div.innerHTML = '<strong>Hello World</strong>';
```

Be cautious with `innerHTML`, as it can expose your site to security risks if user-generated content is inserted.

Alternatively, you can build elements manually for better security:

```javascript
const strong = document.createElement('strong');
strong.innerText = 'Hello World';
div.appendChild(strong);
```

## Removing Elements

Removing elements is straightforward:

```javascript
const elementToRemove = document.querySelector('#element-id');
elementToRemove.remove();
```

Or, use `removeChild`:

```javascript
const parent = document.querySelector('#parent-id');
const child = document.querySelector('#child-id');
parent.removeChild(child);
```

## Accessing and Modifying Attributes

### Using `getAttribute`, `setAttribute`, and `removeAttribute`

* **Get Attribute**:
    
    ```javascript
    const id = element.getAttribute('id');
    ```
    
* **Set Attribute**:
    
    ```javascript
    element.setAttribute('id', 'new-id');
    ```
    
* **Remove Attribute**:
    
    ```javascript
    element.removeAttribute('id');
    ```
    

### Working with Data Attributes

Data attributes start with `data-` and are useful for storing information within HTML elements:

```html
<span data-test="sample" data-longer-name="example"></span>
```

Access them using `dataset`:

```javascript
const span = document.querySelector('span');
console.log(span.dataset.test);  // Output: sample
span.dataset.newName = 'hello';
```

## Managing Classes

### Using `classList`

`classList` provides methods for manipulating classes:

* **Add Class**:
    
    ```javascript
    element.classList.add('new-class');
    ```
    
* **Remove Class**:
    
    ```javascript
    element.classList.remove('old-class');
    ```
    
* **Toggle Class**:
    
    ```javascript
    element.classList.toggle('toggle-class');
    ```
    

## Directly Modifying Styles

Change CSS properties directly via `style`:

```javascript
element.style.color = 'red';
element.style.backgroundColor = 'blue';
```

Remember to camel-case multi-word properties like `backgroundColor`.

## Conclusion

Mastering these DOM manipulation techniques will make your web development journey smoother and more efficient. If you're eager to dive deeper, check out my full JavaScript course for more insights and advanced techniques.

Thank you for reading, and happy coding!