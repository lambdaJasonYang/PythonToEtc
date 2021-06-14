# Combination Sum

Given list and target. Find number of sublists that sum to target, allow repeats.

{% tabs %}
{% tab title="Python" %}
```python
goal = []
def combsum(Arr,target,acc):
    if Arr == [] or target < 0:
        return
    if target == 0:
        goal.append(acc)
        return
    else:
        x = Arr[0]
        IH = Arr[1:]
        combsum(Arr,target-x,[x]+acc)
        combsum(IH,target,acc)

        

```
{% endtab %}
{% endtabs %}

