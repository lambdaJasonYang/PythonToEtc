# Delegates\(Abstract function + lambdas\)

{% tabs %}
{% tab title="C\#" %}
## Monoid as a Delegate 

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

## Actions are Delegates that return Void

```csharp
private void AddEqualsFourtyTwo(int x, string s)
        {
            int y = int.Parse(s);
            Assert.Equal(42, x + y);
        }
Action<int, string> somefunct = AddEqualsFourtyTwo;
somefunct(12, (string)"30");
```

|  |  |
| :--- | :--- |
|  |  |
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

