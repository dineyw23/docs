---
layout: api-command
language: Java
permalink: api/java/type_of/
command: typeOf
---

# Command syntax #

{% apibody %}
any.typeOf() &rarr; string
{% endapibody %}

# Description #

Gets the type of a ReQL query's return value.

The type will be returned as a string:

* `ARRAY`
* `BOOL`
* `DB`
* `FUNCTION`
* `GROUPED_DATA`
* `GROUPED_STREAM`
* `MAXVAL`
* `MINVAL`
* `NULL`
* `NUMBER`
* `OBJECT`
* `PTYPE<BINARY>`
* `PTYPE<GEOMETRY>`
* `PTYPE<TIME>`
* `SELECTION<ARRAY>`
* `SELECTION<OBJECT>`
* `SELECTION<STREAM>`
* `STREAM`
* `STRING`
* `TABLE_SLICE`
* `TABLE`

Read the article on [ReQL data types](/docs/data-types/) for a more detailed discussion. Note that some possible return values from `typeOf` are internal values, such as `MAXVAL`, and unlikely to be returned from queries in standard practice.

__Example:__ Get the type of a string.

```java
r.expr("foo").typeOf().run(conn);
// result: "STRING"
```
