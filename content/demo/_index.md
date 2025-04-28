+++
title = "Demo" 
template = "index.html" 
+++

{% align(align="center") %}
# Demo
{% end %}

# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6

# Typography

[I link to another page.](../)

Using the `{% align(align) %}` shortcode with `center`, `right`, or `justified`, you can change text aligment:

{% align(align="center") %} This text is center-aligned! {% end %}
{% align(align="right") %} This text is right-aligned! {% end %}
{% align(align="justified") %} This text is justified! Justified text needs to span more than one line for it to actually justify as per the CSS specifications{% end %}

# Code Blocks

Code blocks use the Material Dark theme built into Zola.

```rust
// This is some rust code
fn main() {
    someOtherFunction();

    return
}
```

```
If the line in a code block is too long, it will create a scroll bar as demonstrated by this code block.
```

```rust,linenos,linenostart=10,hl_lines=3-4 6
// This codeblock has line numbers and line highlighting
fn someOtherFunction() {
    let foo = "foo";
    let bar = "bar";

    return
}
```