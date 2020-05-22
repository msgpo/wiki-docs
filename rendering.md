---
title: Rendering Pipeline
description: Control how your content is rendered
published: true
date: 2020-05-22T20:43:52.733Z
tags: 
---

# Overview

The rendering pipeline defines how your content is rendered into it's final readable form.

Rendering modules are attached to a core language module. Depending on the editor used, content will go through several **core rendering modules <kbd>CRM</kbd>**. For example, using the Markdown editor will result in the content being transformed through the Markdown CRM, then by the HTML CRM modules.

Each core rendering module can consists of multiple **extension rendering modules <kbd>ERM</kbd>**. These modules extend the capabilities of the core rendering module.

![Rendering Pipeline Diagram](/assets/diagrams/diag-rendering-pipeline.jpg =1000x){.radius-7 .decor-shadow}

Each module can be enabled / disabled individually and configured in the **Administration Area** under the **Rendering** sidebar menu.

# Markdown

## Tabset {.tabset}

### Definition

Converts Markdown content into HTML.

#### Parameters

- **Allow HTML**: Enable HTML tabs in content.
- **Automatically convert links**: Links will automatically be converted into clickable links.
- **Automatically convert line breaks**: Add linebreaks within paragraphs.
- **Typographer**: Enable some language-neutral replacement + quotes beautification.
- **Quotes style**: When typographer is enabled. Double + single quotes replacement pairs. e.g. «»„“ for Russian, „“‚‘ for German, etc.
{.grid-list}


## Abbreviations

### Tabset {.tabset}

#### Definition

Transform abbreviation words into `<abbr>` tags for an expanding definition.

#### Example

```
*[HTML]: Hyper Text Markup Language
*[W3C]:  World Wide Web Consortium
The HTML specification
is maintained by the W3C.
```
will result in

```html
<p>The <abbr title="Hyper Text Markup Language">HTML</abbr> specification
is maintained by the <abbr title="World Wide Web Consortium">W3C</abbr>.</p>
```

#### Parameters

*This module doesn't have any configurable parameters.*


## Emoji

### Tabset {.tabset}

#### Definition

Convert tags into emojis.

#### Example

 `:apple:` will produce :apple:

#### Parameters

*This module doesn't have any configurable parameters.*


## Expand Tabs

### Tabset {.tabset}

#### Definition

Automatically convert tabs into spaces for consistent indentation spacing in HTML.

#### Parameters

- **Tab Width**: The number of spaces to use when converting from tabs.
{.grid-list}


## Footnotes

### Tabset {.tabset}

#### Definition

Generates footnote definitions.

#### Example

See https://github.com/markdown-it/markdown-it-footnote

#### Parameters

*This module doesn't have any configurable parameters.*


## Image Size

### Tabset {.tabset}

#### Definition

Add image dimensions to img tags.

#### Example

```
![test](image.png =100x200)
```
will result in
```html
<p><img src="image.png" alt="test" width="100" height="200"></p>
```

#### Parameters

*This module doesn't have any configurable parameters.*


# HTML

*Coming soon*