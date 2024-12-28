+++
title="Writing Content"
description="Overview of various shortcodes for writing section and page content"
weight=1
+++

## Text Formatting

Metro includes a number of shortcodes to help you format your posts.

### Alignment

Text can be aligned into columns using the  `{% align(align) %}` shortcode. The possible values of algin are "left", "center", "right", and "justified". The shortcode only works with a body of text.

{% align(align="center") %} This text is center-aligned! {% end %}
