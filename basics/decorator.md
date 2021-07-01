---
description: A form of metaprogramming
---

# Decorator

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Second Tab" %}


```python
def decorator(func):
    def wrapper():
        print("begin")
        func()
        print("end")
    return wrapper

#########################
#Version 1
def bleh():
    print("do stuff")
fn = decorator(bleh)
#########################
#Version 2
@decorator
def bleh():
    print("do stuff")
#########################
fn() #OUTPUT: begin  do stuff  end 

```
{% endtab %}
{% endtabs %}



