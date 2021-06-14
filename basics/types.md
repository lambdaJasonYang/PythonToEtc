# Types

## Simple Types

Becoming a super hero is a fairly straight forward process:

{% tabs %}
{% tab title="Python" %}
{% code title="Python" %}
```python
#python
SomeNum = 1  
SomeBool = True
SomeString = "ABC"
SomeChar = "C"
SomeArr = [4,3,2,1]
print(f"output is {SomeString}");

bleh = r"Hello "World""
```
{% endcode %}
{% endtab %}

{% tab title="C\#" %}
```csharp
int SomeNum = 1;
bool SomeBool = true;
string SomeString = "ABC"; //double quotes make strings
char SomeChar = 'C'; //single quote are characters
int[] SomeArr = {4,3,2,1}
int[] F = new int[n];
Console.WriteLine($"output is {SomeString}");

var SomeVar = "hi";
  
//The @ symbol creates a raw string allowing
//double quotes without escaping. 
string bleh = @"Hello, ""World""";
```
{% endtab %}

{% tab title="C++" %}
```cpp
int SomeNum =  1;
bool SomeBool = true;
string SomeString = "ABC";
char SomeChar = 'C';
int[] SomeArr = {4,3,2,1};
int F[10];
std::cout << "output is "  << SomeString << endl;

auto SomeVar = "hi";
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
 Notice C++ and C\# arrays are allocated at compile time and can't be resized. 
{% endhint %}

### Vectors

{% code title="C\#" %}
```csharp
int[] SomeArr = {1,2,3,4}; 
int lastelem = SomeArr[^1];
//SomeArr[^1] == SomeArr[3] , ^1 is -1 in python
SomeArr[2..]
SomeArr[1..3]

List<int> SomeList = new List<int>{1,2,3,4};
foreach (int i in SomeList){
    Console.WriteLine(i);
} 

```
{% endcode %}

### Fibonacci

{% tabs %}
{% tab title="C\#" %}
```csharp
public int fib(int n) {
    if(n == 0){return 0;} //required if statement
    //C# will do an arrayout of bounds 
    //unlike C++ when n = 0
    int[] F = new int[n+1];
    F[0] = 0;
    F[1] = 1; //if n == 0 array out of bounds
    for(int i = 2; i <= n; i++){
        F[i] = F[i-1] + F[i-2];
    }
    return F[n];
            
}


```
{% endtab %}

{% tab title="C++" %}
```cpp
int fib(int n) {
    //int F[n] does not work since n is a variable 
    //and cannot initalize 
    //array F[n] at compile time
    int F[100] = {0};
    F[0] = 0;
    F[1] = 1;
    for(int i = 2; i <= n; i++){
        F[i] = F[i-1] + F[i-2];
    }
    return F[n];
        
}
```
{% endtab %}
{% endtabs %}

{% code title="C\# Linq syntax" %}
```cpp
public int fib(int n) { //recursive using switch case statement
    int output = n switch
    {
        0 => 0,
        1 => 1,
        int x => fib(x-2) + fib(x-1) 
    };
    return output;
        
}
```
{% endcode %}



