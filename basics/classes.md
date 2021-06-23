# Classes



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

