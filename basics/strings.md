# Strings

{% tabs %}
{% tab title="C\#" %}
```csharp
string poem = $"line 1 {System.Environment.NewLine}line 2 ";
//output:
//line 1
//line 2
```
{% endtab %}
{% endtabs %}

```csharp
var world = "World";
var str = String.Format("Hello, {0}", world);
//Hello, World
```

```csharp
public void StringsAreReallyImmutable()
{
    //So here's the thing. Concatenating strings is cool
    //and all. But if you think you are modifying the original
    //string, you'd be wrong. 

    var strA = "Hello, ";
    var originalString = strA; 
    //originalString points to "Hello,"
    var strB = "World";
    strA += strB;
    //allocate new memory that holds "Hello, World"
    //Change strA pointer from "Hello," to "Hello, World"
    Assert.Equal("Hello, World", strA);
    Assert.Equal("Hello, ", originalString);
    
    
    
    //Very important point - if you do this kind
    //of string concatenation in a tight loop, you'll use a lot of memory
    //because the originalString will hang around in memory.
    
    //Best Alternative use StringBuilder
}


```

String formatting

{% tabs %}
{% tab title="C\# Pad\_Left" %}
```csharp
//pads three white space to the left 
var str = string.Format("{0,3:}", "x");
var str = string.Format("{0,3:}", "ab");
var str = string.Format("{0,3:}", "pqr");

//output:
//__x
//_ab
//pqr

//represent _ as whitespace
```
{% endtab %}

{% tab title="Pad\_Right" %}
```csharp
//pads three white space to the right
var str = string.Format("{0,-3:}", "x");
var str = string.Format("{0,-3:}", "ab");
var str = string.Format("{0,-3:}", "pqr");

//output:
//x__  
//ab_
//pqr

//represent _ as whitespace
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Control number of decimal displayed C\#" %}
```csharp
var str = string.Format("{0:.##}", 12.3456);
//12.35

var str = string.Format("{0:.###}", 12.3456);
//12.346

//WARNING IMPLICIT ROUNDING
```
{% endtab %}

{% tab title="Extrapolate decimal places" %}
```csharp
var str = string.Format("{0:.00}", 12.3);
//12.30

var str = string.Format("{0:.000}", 12.3);
//12.300
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Currency Formatting C\#" %}
```csharp
var str = string.Format("{0:n}", 123456);
//123,456.00

var str = string.Format("{0:c}", 123456);
//$123,456.00

```
{% endtab %}
{% endtabs %}

```csharp
using System.Globalization;
var str = string.Format("{0:t}", DateTime.Parse("12/16/2011 2:35:02 PM", CultureInfo.InvariantCulture));
//2:35 PM

var str = string.Format("{0:t m}", DateTime.Parse("12/16/2011 2:35:02 PM", CultureInfo.InvariantCulture));
//P 35
```

### 

### Dont Concatenate, use String builder

```csharp
var strBuilder = new System.Text.StringBuilder();
strBuilder.Append("The ")
          .Append("little ")
          .Append("fox");
var str = strBuilder.ToString();
//The little fox
```



