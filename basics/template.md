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
template<typename T>
class bleh {
    T someVar;
    public: 
        bleh( T val = {}) :  someVar(val) {}
        
        T get() { return someVar; }
        void set(T value){ someVar = value }
}
```
{% endtab %}
{% endtabs %}





