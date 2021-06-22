# Nulls

```csharp
public void AWayNotToCheckThatAnObjectIsNull()
{
  object obj = null;
  Assert.True(obj.Equals(null));
}
```

