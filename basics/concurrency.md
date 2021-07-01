# Concurrency

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Second Tab" %}
## Thread

```cpp
void func(){
    std::cout << "hey" << std::endl;
}
int main(){
    std::thread t1(func);
    t1.join();
    return 0;
}
```
{% endtab %}
{% endtabs %}



