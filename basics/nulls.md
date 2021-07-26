# Nulls and Maybe Functor

{% tabs %}
{% tab title="C\#" %}
```csharp
//DO NOT DO THIS
object obj = null;
bool x = obj.Equals(null); //throws Null Exception

//DO THIS
bool x = obj == null;

```

```csharp
int i = 0;
//i = null; //You can't do this

int? nullableInt = null; //Maybe functor 
//but you can do this
```



```csharp
int? nullableInt = null;

//the below 2 expression are the same
int x = nullableInt ?? 42; 
int x = nullableInt != null ? nullableInt : 42
//if nullableInt is not null, x is set as nullableInt else it is 42
Assert.Equal(42, x);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

