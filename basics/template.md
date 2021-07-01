# Template

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="C++" %}
## Templates

```cpp
#include <iostream>
template<typename T>
T concat(T a, T b){
    return a + b;
}

```

```cpp
//template for class
template<typename T>
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
    bleh<int> x(0);
    bleh<const char*> y("xyz");
}
```
{% endtab %}
{% endtabs %}





