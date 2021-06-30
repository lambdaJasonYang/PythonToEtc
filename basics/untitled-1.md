# Delegates\(Abstract function + lambdas\)

{% tabs %}
{% tab title="C\#" %}
## Overview

```csharp
delegate int bleh(string x, double y);
Action<string, double> blah;
Func<string,double,int> bluh;
Predicate<int> bloh;
```

## Monoid as a Delegate 

```csharp
delegate int Monoid(int lhs, int rhs);
//(int,int) -> int
//any function that fits the above type signature can be assigned

Monoid bleh = new Monoid(math.Add)

//we can use delegates as parameters
private void SomeFunction( Monoid duhr){
    duhr(2,4);
  }  
  
bleh = bleh + subtraction;
bleh = bleh + addition;

```

## Delgates and Lambdas

```csharp
public class bleh{
	public delegate void TestDelegate();
	public TestDelegate myfunct;
	public bleh(){
		myfunct = delegate(){   //this is the lambda function
					Console.WriteLine(3);
												};
												
	}	
}
                
```

## Actions are Delegates that return Void

```csharp
private void AddEqualsFourtyTwo(int x, string s)
        {
            int y = int.Parse(s);
            Assert.Equal(42, x + y);
        }
Action<int, string> somefunct = AddEqualsFourtyTwo;
somefunct(12, (string)"30");
```

## Func are Delegates that can return any type

{% hint style="info" %}
Last generic parameter of Func is the return type 
{% endhint %}

```csharp
//Func<string> means () -> string
//last generic parameter is string meaning the return type is string
Func<string> printMonth = FirstMonth;
Assert.Equal("January", printMonth());

//Func<int, int, string> means (int, int) -> string
Func<int, int, string> a = Add;
Assert.Equal("2", a(1, 1));

```

## Predicate are Delegates that return bool

{% hint style="danger" %}
Predicate can only take 1 generic parameter unlike the delegates above
{% endhint %}

```text
bool IntEqualsFourtyTwo = (int x) => { return x == 42};
Predicate<int> i = (Predicate<int>)IntEqualsFourtyTwo;
Assert.True(i(42));
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



