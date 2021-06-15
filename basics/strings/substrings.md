# Substrings

```csharp
string str = "hello";
string str2 = str.Substring(1,3);
//starts inclusive [1,1+3) = [1,4)

//output:
//ell
```

```csharp
string str = "hello"
string str2 = str[0] //ERROR
Assert.Equal("B", str[0]); //ERROR

char str2 = str[0] //CORRECT
Assert.Equal('B', str[0]); //CORRECT
```

