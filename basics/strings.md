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
public void StringsAreReallyImmutable()
{
    //So here's the thing. Concatenating strings is cool
    //and all. But if you think you are modifying the original
    //string, you'd be wrong. 

    var strA = "Hello, ";
    var originalString = strA;
    var strB = "World";
    strA += strB;
    Assert.Equal("Hello, World", strA);
    Assert.Equal("Hello, ", originalString);

    //What just happened? Well, the string concatenation actually
    //takes strA and strB and creates a *new* string in memory
    //that has the new value. 
    //It does *not* modify the original string.
    //This is a very important point - if you do this kind
    //of string concatenation in a tight loop, you'll use a lot of memory
    //because the original string will hang around in memory until the
    //garbage collector picks it up. Let's look at a better way
    //when dealing with lots of concatenation
}


public void YouDoNotNeedConcatenationToInsertVariablesInAString()
{
    var world = "World";
    var str = String.Format("Hello, {0}", world);
    Assert.Equal("Hello, World", str);
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

>

