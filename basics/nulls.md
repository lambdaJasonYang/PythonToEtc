# Nulls

```csharp
public void AWayNotToCheckThatAnObjectIsNull()
{
  object obj = null;
  Assert.False(obj.Equals(null));
}
```

