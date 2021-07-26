# Interfaces and Typeclasses

Typeclasses are constraints that must be implemented by the target type  
Interfaces are constraints that must be implemented by the target class.

{% tabs %}
{% tab title="C\#" %}
```text

```
{% endtab %}

{% tab title="Haskell" %}
```haskell
class Eq a where
  (==) :: a -> a -> Bool
  (/=) :: a -> a -> Bool
  -- let's just implement one function in terms of the other
  x /= y = not (x == y)
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
interface MyProps{
  label : string;
  price?: number; //The ? marks the parameter as optional
  [key: string]: any //allows us to add any additional property
}
```
{% endtab %}
{% endtabs %}

