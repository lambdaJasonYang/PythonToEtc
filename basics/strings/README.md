# Strings

{% tabs %}
{% tab title="First Tab" %}
## OS independent new Line

```csharp
string poem = $"line 1 {System.Environment.NewLine}line 2 ";
//output:
//line 1
//line 2
```

## String formatting

```csharp
var world = "World";
var str = String.Format("Hello, {0}", world);
//Hello, World
```

```csharp
public void StringConcatBadPractice()
{
    //if you think you are modifying the original
    //string, you'd be wrong. 
    var strA = "Hello, ";
    var originalString = strA;//originalString points to "Hello,"
    var strB = "World";
    strA += strB; //CONCAT
    //allocate new memory that holds "Hello, World"
    //Change strA pointer from "Hello," to "Hello, World"
    Assert.Equal("Hello, World", strA);
    Assert.Equal("Hello, ", originalString);
    
    //Very important point - if you do this kind
    //of string concatenation in a tight loop, you'll use a lot of memory
    //because the originalString will hang around in memory.
    
    //BEST ALTERNATIVE USE StringBuilder
}


```

## String builder

```csharp
var strBuilder = new System.Text.StringBuilder();
strBuilder.Append("The ")
          .Append("little ")
          .Append("fox");
var str = strBuilder.ToString();
//The little fox
```

```csharp
var strBuilder = new System.Text.StringBuilder();
strBuilder.AppendFormat("{0} {1} {2}", "The", "quick", "brown")
		  		.AppendFormat("{0} {1}.", "lazy", "dog");
var str = strBuilder.ToString();
//The quick brownlazy dog.
```

## Padding format

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

```csharp
var str = string.Format("{0:.##}", 12.3456);
//12.35

var str = string.Format("{0:.###}", 12.3456);
//12.346

//WARNING IMPLICIT ROUNDING
```

```csharp
var str = string.Format("{0:.00}", 12.3);
//12.30

var str = string.Format("{0:.000}", 12.3);
//12.300
```

## Currency format

```csharp
var str = string.Format("{0:n}", 123456);
//123,456.00

var str = string.Format("{0:c}", 123456);
//$123,456.00

```

## Date format

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
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



