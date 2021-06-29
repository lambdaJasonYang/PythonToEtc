---
description: Classes are basically custom types
---

# Classes



{% tabs %}
{% tab title="First Tab" %}


class MyAnimals { public const int Legs = 2;

```csharp
class Animal
{
    public const int Legs = 4;

    public int LegsInAnimal()
    {
        return Legs;
    }
}

class MyAnimals
{
    public const int Legs = 2;

    public class Bird : Animal
    {
        public int LegsInBird()
        {
            return Legs;
        }
    }
}
Assert.Equal(4, bird.LegsInBird());
//Bird is a nested class of MyAnimals and a subclass that inherits Animal
//Bird.Legs will return 4 from its Animal parent
//Inheritance takes priority over lexical scope in the nested class
```

{% hint style="info" %}
Inheritance takes priority over lexical scope in the nested class
{% endhint %}

```csharp
class Foo3
{
    private bool _boom = true;
    public bool Internal { get => _boom; set { _boom = value; } }
    //set has implicit parameter value

    public void Do()
    {
        if (_boom)
        {
            throw new InvalidOperationException(nameof(Do));
        }
    }
}

public void UseAccessorsToReturnInstanceVariables()
{
    var foo = new Foo3();
    //notice foo.Internal = ??
    // the = assignment calls the set function, set(value){_boom = value}
    
    foo.Internal = false;
    
    //foo.Internal without the = aka without assignment 
    //will call, get => _boom;  
    Console.log(foo.Internal)
    
    foo.Do();
}

```

{% hint style="info" %}
class method set  has implicit parameter, value 
{% endhint %}
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



