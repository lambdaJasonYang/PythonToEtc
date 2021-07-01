---
description: A form of metaprogramming
---

# Decorator

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Python" %}


```python
def decorator(func):
    def wrapper(*args, **kwargs): #arguments of the target function
        print("begin")
        func(*args, **kwargs)
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

## Parameterized Decorators

```python
def decorator_params(*decorator_args, **decorator_kwargs):
    def decorator(func):
        def wrapper(*args, *kwargs):
            print("begin")
            func(*decorator_args, **decorator_kwargs,*args, **kwargs)
            print("end")
        return wrapper
#################################
@decorator_params(1,2)
def bleh(x,y,z):
    print(f"{x} {y} {z}")
#################################
bleh(3) #OUTPUT: 1 2 3
```
{% endtab %}
{% endtabs %}



