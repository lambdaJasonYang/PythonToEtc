---
description: Classes are basically custom types
---

# Classes, Enums, Inheritance

Classes are simply just a tuple of primitive data types

{% tabs %}
{% tab title="C\#" %}




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

{% tab title="Typescript" %}
## Interface

many times this is used to pass props

```typescript
interface MyProps{
  label : string;
  price?: number; //The ? marks the parameter as optional
  [key: string]: any //allows us to add any additional property
}

```
{% endtab %}

{% tab title="Haskell" %}
```haskell
-- Enumeration types
data Bool = True | False
data Color = Red | Green | Blue

-- Record types that contain fields
data Vector2d = MakeVector Double Double
data Person = Person Int String

-- Parameterized types. Note the type parameter `a`
data PairOf a = TwoValues a a

-- Recursive types
data IntList = Empty | Node Int IntList

-- Complex types which combine many of these features
data Maybe a = Nothing | Just a
data Either a b = Left a | Right b
data List a = Nil | Cons a (List a)             -- This is equivalent to the built-in [a] type
data Tree a = Leaf a | Node a (Tree a) (Tree a)
data MultiTree a = MultiTree a [MultiTree a]     -- Note the list
```
{% endtab %}
{% endtabs %}



