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
```

