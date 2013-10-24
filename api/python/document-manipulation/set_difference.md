---
layout: api-command 
language: Python
permalink: api/python/set_difference/
command: set_difference 
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/python/document-manipulation/set_difference.md
related_commands:
    union: union/
    difference: difference/
    set_insert: set_insert/
    set_union: set_union/
    set_intersection: set_intersection/
---

# Command syntax #

{% apibody %}
array.set_difference(array) &rarr; array
{% endapibody %}

# Description #

Remove the elements of one array from another and return them as a set (an array with
distinct values).

__Example:__ Check which pieces of equipment Iron Man has, excluding a fixed list.

```py
r.table('marvel').get('IronMan')['equipment'].set_difference(['newBoots', 'arc_reactor']).run(conn)
```