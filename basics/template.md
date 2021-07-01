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
//typename T = int, means default template type is int
//notice we can use non-templates like int arrlen as well
template<typename T=int, int arrlen = 10>
class bleh {
    T someVar;
    int arr[arrlen]
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

```text
T{} is instantiation of default value for type T
template<typename T=int> is default template type is int
```
{% endtab %}
{% endtabs %}





