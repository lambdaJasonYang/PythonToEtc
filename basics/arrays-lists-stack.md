# Arrays Lists Stack

```csharp
var empty_array = new object[] { };
Assert.Equal(typeof(object[]), empty_array.GetType());

//Note that you have to explicitly check for subclasses
Assert.True(typeof(Array).IsAssignableFrom(empty_array.GetType()));

var array = new[] { 42 };
Assert.True(array.IsFixedSize);
Assert.Throws(typeof(System.IndexOutOfRangeException), delegate () { array[1] = 13; });
```

```csharp
List<int> dynamicArray = new List<int>();
dynamicArray.Add(42);
Assert.Equal((new int[] { 42 }), dynamicArray.ToArray());
```

## Slicing

```csharp
var array = new[] { "peanut", "butter", "and", "jelly" };

Assert.Equal(new string[] { "peanut", "butter" }, array.Take(2).ToArray());
Assert.Equal(new string[] { "butter", "and" }, array.Skip(1).Take(2).ToArray());
```

## Stack

```csharp
var array = new[] { 1, 2 };
var stack = new Stack(array); //push array in reverse order
//stack is {2, 1}
stack.Push("last");
Assert.Equal(new Object[] { "last", 2, 1 }, stack.ToArray());
var poppedValue = stack.Pop();
Assert.Equal("last", poppedValue);
Assert.Equal(new Object[] { 2, 1 }, stack.ToArray());
```

## LinkedList methods

```csharp
var array = new[] { "Hello", "World" };
var list = new LinkedList<string>(array);

list.AddFirst("Say");
Assert.Equal(new String[] { "Say", "Hello", "World" }, list.ToArray());

list.RemoveLast();
Assert.Equal(new String[] { "Say", "Hello" }, list.ToArray());

list.RemoveFirst();
Assert.Equal(new String[] { "Hello" }, list.ToArray());

list.AddAfter(list.Find("Hello"), "World");
Assert.Equal(new String[] { "Hello", "World" }, list.ToArray());
```

