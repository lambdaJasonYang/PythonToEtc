# Delegates\(Abstract function + lambdas\)

{% tabs %}
{% tab title="C\#" %}


```csharp
delegate int Monoid(int lhs, int rhs);
//(int,int) -> int
//any function that fits the above type signature can be assigned

Monoid bleh = new Monoid(math.Add)

//we can use delegates as parameters
private void SomeFunction( Monoid duhr){
    duhr(2,4);
  }  

```

## Delgates and Lambdas

```csharp
var lambdaFunct = delegate (int x){ return x; };
var lambdaFunct = (int x) => {return x}
                
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

