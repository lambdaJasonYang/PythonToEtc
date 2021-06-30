# Array Methods

{% tabs %}
{% tab title="First Tab" %}
## Finding first Elem in Array

```csharp
string[] countries = new string[] { "Greece", "Spain", "Uruguay", "Japan" };
Assert.Equal("Spain", Array.Find(countries, StartsWithS));
```

## Check Elem in Array

```csharp
bool checkGreece = countries.Contains("Greece") //returns true
```

```csharp
bool checkGreece = countries.Any(x => x.Contains("Greece")); 
//Check if any of your words contain 'ei'
```

## Filter

```csharp
string[] result = countries.Where(x => x.Contains("a")).ToArray();
//{"Spain","Uruguay","Japan"}
```

## Masking - returns array of bools

```csharp
var numbers = new[] { 1, 2, 3, 4 };
var result = numbers.Select(x => x > 2).ToArray();

//What values should be in array?
Assert.Equal(new bool[] { false, false, true, true }, result);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



