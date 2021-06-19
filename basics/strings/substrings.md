# Substrings

{% tabs %}
{% tab title="C\#" %}
```csharp
string str = "hello";
string str2 = str.Substring(1,3);
//starts inclusive [1,1+3) = [1,4)

//output:
//ell

string str3 = str.Substring(1); //[1,inf)
//ello
```
{% endtab %}
{% endtabs %}

```csharp
string str = "hello"
string str2 = str[0] //ERROR
Assert.Equal("B", str[0]); //ERROR
//RETURNS CHARACTER NOT STRING

char str2 = str[0] //CORRECT
Assert.Equal('B', str[0]); //CORRECT
```

{% hint style="danger" %}
someString\[0\] will return a character type 
{% endhint %}

{% tabs %}
{% tab title="Split string C\#" %}
```csharp
var str = "Sausage Egg Cheese";
string[] words = str.Split();
Assert.Equal(new[] { "Sausage", "Egg", "Cheese" }, words);


var str = "the:rain:in:spain";
string[] words = str.Split(':');
Assert.Equal(new[] { "the", "rain", "in", "spain" }, words);
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Regex C\#" %}
```csharp
var str = "the:rain:in:spain";
var regex = new System.Text.RegularExpressions.Regex(":");
string[] words = regex.Split(str);
Assert.Equal(new[] { "the","rain","in","spain" }, words);
```
{% endtab %}
{% endtabs %}

