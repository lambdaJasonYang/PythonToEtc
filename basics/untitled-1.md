# Delegates\(Abstract function + lambdas\)

{% tabs %}
{% tab title="C\#" %}
## Overview

Using the "delegate" keyword first defines the function type bleh.

```csharp
delegate int bleh(string x, double y);// first define bleh type
bleh pointTofunc = Thefunc; 
//bleh contains the set of all functions with 
//type (string,double) -> int

//Unlike bleh, Action<..> Funct<..> Predicate<..> 
//do not need to be initialized
Action<string, double> blah;
//Action<string,double> contains the set of all functions with
//type (string,double) -> void

Func<string,double,int> bluh;
//Func<string,double,int> contains the set of all functions with
//type (string,double) -> int

Predicate<int> bloh;
//Predicate<int> contains the set of all functions with
//type (int) -> bool

bleh~Action~Func~Predicate
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

## Delgates and sorta-Lambdas

```csharp
public class bleh{
  public delegate int IntLambdaType(int x); //Similar to Haskell type init
  public IntLambdaType e = delegate(int a){return a;};

}
                
```

{% hint style="info" %}
Notice delegate is a like a type constructor that creates the IntLambdaType.

Unlike delegates which has to be initalized  
Actions Func Predicate can be used as types directly
{% endhint %}

## Actions are Functions that return Void

```csharp
private void AddEqualsFourtyTwo(int x, string s)
        {
            int y = int.Parse(s);
            Assert.Equal(42, x + y);
        }
Action<int, string> somefunct = AddEqualsFourtyTwo;
somefunct(12, (string)"30");
```

## Func are Functions that return type of last param

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

## Predicate are Functions that return bool

{% hint style="danger" %}
Predicate can only take 1 generic parameter unlike the delegates above
{% endhint %}

```csharp
bool IntEqualsFourtyTwo = (int x) => { return x == 42};
Predicate<int> i = (Predicate<int>)IntEqualsFourtyTwo;
Assert.True(i(42));
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



