# Nulls

```csharp
public void BadWayToCheckNull()
{
  object obj = null;
  Assert.False(obj.Equals(null));
  //the assertion passes
  //unexpected behavior is allowed
}

//Proper way to check if an object is null
public void GoodWayToCheckNull() 
{
 object obj = null; 
 Assert.Null(obj); 
 //assertion passes
}
 
public void  AnotherWayToCheckNull()
{
 object obj = null;
 Assert.True(obj == null);
}
```

