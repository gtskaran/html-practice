## HTML5 Typography Tags

| Tag | Purpose | Typical Use |
|-----|---------|--------------|
| `<h1>` – `<h6>` | Section headings, hierarchical | Page title (`<h1>`), sub‑sections (`<h2>`‑`<h3>`) |
| `<p>` | Paragraph of text | Main body copy |
| `<blockquote>` | Long quotation | Citing a source |
| `<cite>` | Title of a work | Inside `<blockquote>` or `<footer>` |
| `<abbr>` | Abbreviation | `<abbr title="HyperText Markup Language">HTML</abbr>` |
| `<address>` | Contact information | Footer or author bio |
| `<pre>` | Pre‑formatted text | Code snippets |
| `<code>` | Inline code | `<code>var x = 10;</code>` |
| `<samp>` | Sample output | `<samp>Result: 42</samp>` |
| `<kbd>` | Keyboard input | `<kbd>Ctrl + C</kbd>` |
| `<mark>` | Highlighted text | `<mark>important</mark>` |
| `<small>` | Smaller print | Legal disclaimer |
| `<strong>` | Strong importance | **Bold** semantics |
| `<em>` | Emphasis | *Italic* semantics |
| `<del>` / `<ins>` | Deleted / inserted text | Revision tracking |
| `<sup>` / `<sub>` | Superscript / subscript | Math, footnotes |

---

## Minimal CSS for Clean Typography

```css
/* Base font and line height */
html {
  font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  line-height: 1.6;
  font-size: 100%; /* 16px default */
}

/* Headings */
h1, h2, h3, h4, h5, h6 {
  margin-top: 1.5em;
  margin-bottom: 0.5em;
  line-height: 1.2;
}
h1 { font-size: 2.25rem; }
h2 { font-size: 1.75rem; }
h3 { font-size: 1.5rem; }
h4 { font-size: 1.25rem; }
h5 { font-size: 1rem; }
h6 { font-size: 0.875rem; }

/* Paragraphs */
p {
  margin: 0 0 1em;
}

/* Blockquote */
blockquote {
  margin: 1.5em 0;
  padding-left: 1em;
  border-left: 4px solid #ccc;
  color: #555;
  font-style: italic;
}

/* Code */
pre, code, kbd, samp {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
  background: #f5f5f5;
  border-radius: 4px;
}
pre {
  padding: 1em;
  overflow-x: auto;
}
code {
  padding: 0.2em 0.4em;
}

/* Small & mark */
small { font-size: 0.85em; color: #666; }
mark { background: #fffb8f; }

/* Abbreviation */
abbr[title] {
  border-bottom: 1px dotted #999;
  cursor: help;
}

/* Address */
address {
  font-style: normal;
  line-height: 1.4;
}
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Typography Demo</title>
  <style>
    /* Insert the CSS from above */
    html {font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; line-height:1.6;}
    h1{font-size:2.25rem;} h2{font-size:1.75rem;} h3{font-size:1.5rem;}
    h1,h2,h3{margin-top:1.5em;margin-bottom:0.5em;line-height:1.2;}
    p{margin:0 0 1em;}
    blockquote{margin:1.5em 0;padding-left:1em;border-left:4px solid #ccc;color:#555;font-style:italic;}
    pre,code,kbd,samp{font-family:"SFMono-Regular",Consolas,"Liberation Mono",Menlo,monospace;background:#f5f5f5;border-radius:4px;}
    pre{padding:1em;overflow-x:auto;}
    code{padding:0.2em 0.4em;}
    small{font-size:0.85em;color:#666;}
    mark{background:#fffb8f;}
    abbr[title]{border-bottom:1px dotted #999;cursor:help;}
    address{font-style:normal;line-height:1.4;}
  </style>
</head>
<body>

<h1>Understanding HTML5 Typography</h1>

<p>HTML5 provides a set of semantic tags that describe the structure and meaning of text. Using them correctly improves accessibility and SEO.</p>

<h2>Quotes and Citations</h2>

<blockquote>
  “The only way to do great work is to love what you do.” 
  <cite>— Steve Jobs</cite>
</blockquote>

<h2>Code Samples</h2>

<p>Inline code: <code>let total = price * quantity;</code></p>

<pre><code>
function greet(name) {
  console.log(`Hello, ${name}!`);
}
greet('Alice');
</code></pre>

<h2>Special Text</h2>

<p>Use <abbr title="HyperText Markup Language">HTML</abbr> for markup, <strong>strong importance</strong>, and <em>emphasis</em>. Highlight <mark>key terms</mark> and add footnotes<sup>1</sup>.</p>

<p><small>© 2026 Example Corp. All rights reserved.</small></p>

<address>
  Example Corp.<br>
  123 Main St., Anytown, USA<br>
  <a href="mailto:info@example.com">info@example.com</a>
</address>

</body>
</html>
```

---

## Exercises

1. **Create a blog post**  
   - Use at least three heading levels.  
   - Include a blockquote with a citation.  
   - Add an inline `<code>` snippet and a `<pre>` block for a short script.  

2. **Style a definition list**  
   - Write a `<dl>` with three `<dt>`/`<dd>` pairs (e.g., terms and definitions).  
   - Add CSS to give the terms a left‑border and a subtle background.  

3. **Responsive typography**  
   - Add a media query that reduces heading sizes by 20 % on screens narrower than 600 px.  
   - Test the page on a mobile device to verify readability.  

These tasks reinforce the tags, CSS basics, and responsive design. Happy coding!
