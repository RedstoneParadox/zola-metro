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

# Shortcodes

Using the `{% align(align) %}` shortcode with `center`, `right`, or `justified`, you can change text aligment:

{% align(align="center") %} This text is center-aligned! {% end %}
{% align(align="right") %} This text is right-aligned! {% end %}
{% align(align="justified") %} This text is justified! Justified text needs to span more than one line for it to actually justify as per the CSS specifications{% end %}