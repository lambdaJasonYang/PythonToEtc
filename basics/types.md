# Types

## Simple Types

Becoming a super hero is a fairly straight forward process:

{% code title="Python" %}
```python
#python
SomeNum = 1  
SomeBool = True
SomeString = "ABC"
SomeChar = "C"
SomeArr = [4,3,2,1]
print(f"output is {SomeString}");
```
{% endcode %}

{% code title="CSharp" %}
```bash
int SomeNum = 1;
bool SomeBool = true;
string SomeString = "ABC";
char SomeChar = 'C';
int[] SomeArr = {4,3,2,1}
Console.WriteLine($"output is {SomeString}");

var SomeVar = "hi";
```
{% endcode %}

{% code title="C++" %}
```cpp
int SomeNum =  1;
bool SomeBool = true;
string SomeString = "ABC";
char SomeChar = 'C';
int[] SomeArr = {4,3,2,1};
std::cout << "output is "  << SomeString << endl;

auto SomeVar = "hi";
```
{% endcode %}

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

### Vectors

{% code title="" %}
```cpp
    int fib(int n) {
        //int F[n] does not work since n is a variable and cannot initalize 
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
{% endcode %}

