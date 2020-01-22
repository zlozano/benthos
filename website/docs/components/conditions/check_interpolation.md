---
title: check_interpolation
type: condition
---

<!--
     THIS FILE IS AUTOGENERATED!

     To make changes please edit the contents of:
     lib/condition/check_interpolation.go
-->


```yaml
check_interpolation:
  condition: {}
  value: ""
```

Resolves a string containing
[function interpolations](/docs/configuration/interpolation#functions) and then tests
the result against a child condition.

For example, you could use this to test against the size of a message batch:

``` yaml
check_interpolation:
  value: ${!batch_size}
  condition:
    number:
      operator: greater_than
      arg: 1
```

