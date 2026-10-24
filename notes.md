# HTTP observations (Lab 4, Task 1)

| Question | My answer |
|----------|-----------|
| Request method for index.html |GET|
| Status code with Disable cache ticked | 200 |
| Status code on a normal reload | 304 |
| Status code for /nothing-here.html | 404 |
| Value of the Content-Type response header | text/html; charset=utf-8  |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |

## Why is this address http and not https?

Localhost traffic stays entirely inside your own computer and never travels across the public internet where it could be intercepted. Because of this isolation, there is no risk of network eavesdropping, making the encryption and security certificates of HTTPS unnecessary for basic local development.

## Specificity

A more specific CSS selector overrides a less specific one because the browser calculates a strict numeric weight score for each rule, prioritizing localized declarations matching exact attributes or IDs over general, broad element definitions.

## Selectors I used

| Selector kind | Example from my CSS |
| :--- | :--- |
| **Element** | `body` |
| **Class** | `.hero` |
| **ID** | `#main` |
| **Grouping (comma)** | `h1, h2, h3` |
| **Descendant (space)** | `.nav-list a` |
| **Child (>)** | `main > section` |
| **Adjacent sibling (+)** | `h1 + p` |
| **Compound** | `a.active` |
| **Attribute** | `a[href^="http"]` |
| **Pseudo-class** | `a:hover` |
| **Pseudo-element** | `::placeholder` |
