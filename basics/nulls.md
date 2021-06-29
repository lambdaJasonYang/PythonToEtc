# Nulls and Maybe Functor

{% tabs %}
{% tab title="First Tab" %}
```csharp
public void BadWayToCheckNull()
{
  object obj = null;
  Assert.False(obj.Equals(null));
  Assert.True(obj.Equals(null)); 
  //None of the above passes
  //why?
  //We are trying to call a method under a null object
  //it will throw an Null Reference exception
}

//Proper way to check if an object is null
public void GoodWayToCheckNull() 
{
 object obj = null; 
 Assert.Null(obj); 
 //assertion passes
}
 
public void AnotherWayToCheckNull()
{
 object obj = null;
 Assert.True(obj == null);
 //assertion passes
}
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

