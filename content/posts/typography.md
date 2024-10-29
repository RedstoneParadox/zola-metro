+++
title="Typography"
description="Overview of various typography and formatting shortcodes"
date=2024-10-29

[taxonomies]
tags = ["how-to"]
+++

Metro includes a number of shortcodes to help you format your posts.

# Alignment

Text can be aligned into columns using the  `{% align(align) %}` shortcode. The possible values of algin are "left", "center", "right", and "justified". The shortcode only works with a body of text.

{% align(align="center") %} This text is centered! {% end %}