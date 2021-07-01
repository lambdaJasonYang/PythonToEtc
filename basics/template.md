# Template

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="C++" %}
## Templates

```cpp
#include <iostream>
//notice we can use non-template params as well
template<typename T, int x = 5>
T dosomething(T a){
    return a + 5;
}

```

```cpp
//template for class
//typename T = int, means default template type is int
template<typename T=int>
class bleh {
    T someVar;
    public: 
        bleh( T val = T{}) :  someVar(val) {}
        // T val = T{} means val is set to the default variable of type T
        //default value for int is 0     
        T get() { return someVar; }
        void set(T value){ someVar = value }
}

//class method outside of class block
template<typename T>
void bleh<T>::blehMethod(T param){ someVar = param} 

int main(){
    bleh<> x(0); //same as bleh<int> due to default template type T=int
    bleh<const char*> y("xyz");
}
```

{% hint style="info" %}
```
T{} is instantiation of default value for type T
```
{% endhint %}

## Nested templates aka Functors

```text
T{} is instantiation of default value for type T
```
{% endtab %}
{% endtabs %}





