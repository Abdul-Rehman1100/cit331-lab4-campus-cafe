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


| # | File/element | Problem found | How I detected it | Fix |
|---|---|---|---|---|
| 1 | bugs.html | Wrong CSS filename in the stylesheet link (`href="style.css"`). | Network | Change `href="style.css"` to `href="bugs.css"`. |
| 2 | bugs.html | Missing document language attribute on the `<html>` tag. | Validator | Change `<html>` to `<html lang="en">`. |
| 3 | bugs.html | Heading level structural error: skips directly from `<h1>` to `<h4>`. | Accessibility tree | Change `<h4>` to `<h2>`. |
| 4 | bugs.html | Navigation uses a generic `<div>` wrapper instead of an accessibility landmark. | Lighthouse | Replace the navigation wrapper with `<nav aria-label="Main">` and its closing `</nav>`. |
| 5 | bugs.html | Logo image element has no alternative text attribute (`alt`). | Lighthouse | Add `alt="Campus Café logo"` to the image. |
| 6 | bugs.html | Label points to the wrong field because `for="mail"` does not match `id="email"`. | Form label test | Change `for="mail"` to `for="email"`. |
| 7 | bugs.css | Invalid CSS color property name (`colour: #ffffff;`). | Styles pane | Change `colour` to `color`. |
| 8 | bugs.css | Missing CSS statement terminator semicolon (`;`) after `background: #0b1f3a`. | Styles pane | Add `;` after `background: #0b1f3a`. |
| 9 | bugs.css | CSS class selector `.notes` does not match the singular `class="note"` used in the HTML. | Elements panel | Change `.notes` to `.note`. |
| 10 | bugs.html | Submit button lacks an explicit functional action type attribute. | Code inspection | Add `type="submit"` to the `<button>` element. |

