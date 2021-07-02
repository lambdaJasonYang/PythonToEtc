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
    t1.join(); //you must join or detach a thread
    //process will terminate if you dont
    return 0;
}
```
{% endtab %}
{% endtabs %}



