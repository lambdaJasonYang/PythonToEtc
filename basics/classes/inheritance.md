# Inheritance

```csharp
public class Dog
{
    public string Name { get; set; }

    public Dog(string name)
    {
        Name = name;
    }

    // For a method/function to be overridden by sub-classes, it must be virtual.
    public virtual string Bark()
    {
        return "WOOF";
    }
}

public class Chihuahua : Dog
{
    // The only way to "construct" a Dog is to give it a name. Since a 
    // Chihuahua 'is a Dog' it must conform to a public/protected
    // constructor. Since the only public/protected constructor for a 
    // dog requires a name, a public/protected constructor must also
    // require a Name.
    public Chihuahua(string name) : base(name)
    {
    }

    //Unless it doesn't. You have to call the base constructor at some point
    //with a name, but you don't have to have your class conform to that spec:
    public Chihuahua() : base("Ima Chihuahua")
    {
    }

    // For a Chihuahua to do something different than a regular "Dog"
    // when called to "Bark", the base class must be virtual and the
    // derived class must declare it as "override".
    public override string Bark()
    {
        return "yip";
    }

    // A derived class can have have methods/functions or properties
    // that are new behaviors altogether.
    public string Wag()
    {
        return "Happy";
    }
}
```

