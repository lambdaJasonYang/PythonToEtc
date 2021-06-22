# Nulls

```csharp
public void BadWayToCheckNull()
{
  object obj = null;
  Assert.False(obj.Equals(null));
  Assert.True(obj.Equals(null)); 
  //None of the above passes
  //why?
  //We are trying to call a method under a null object
  //it will throw an Null Reference exception
}

//Proper way to check if an object is null
public void GoodWayToCheckNull() 
{
 object obj = null; 
 Assert.Null(obj); 
 //assertion passes
}
 
public void AnotherWayToCheckNull()
{
 object obj = null;
 Assert.True(obj == null);
 //assertion passes
}
```

