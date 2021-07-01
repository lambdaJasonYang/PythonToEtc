# Template

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="C++" %}
## Templates parameters 

Usually we have `typename T` as a template parameter but we can also have real types like int.  
`template<...template params...>`  and the params are the generic types

```cpp
#include <iostream>
//typename T and int x are template parameters
template<typename T, int x = 5>
T dosomething(T a){
    return a + x;
}
```

## Functors, Templates as template parameters

aka nested templates

```text
template<typename T, template <typename> class Container>
```

## Templates with Classes

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
{% endtab %}
{% endtabs %}







