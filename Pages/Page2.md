---
fname: Sandip Patel
layout: demo_template
theme: jekyll-theme-cayman
---

# User Guide

The Demo User Guide provides documentation for users of TWT Certification topics. See [Getting Started](https://sandy-patel02.github.io/New-Product-Documentation/Page1.html) for an introductory tutorial. You can jump directly 
to a page listed below, or use the next and previous buttons in the navigation bar at the top of the page to move through the documentation in order.

|Name of the passengers|Age |
|----------------------|----| {% for item in site.data.titanic %}
|{{item.Name}}|{{ item.Age }}| {% endfor %}