# Gotchas



```csharp
        public void DoubleQuotedStringsAreStrings()
        {
            var str = "Hello, World";
            Assert.Equal(typeof(string), str.GetType());
        }
        //passes


        public void SingleQuotedStringsAreCharacters()
        {
            var str = 'H';
            Assert.Equal(typeof(char), str.GetType());
        }
        //passes
```

## Strings and Delegates are immutable

String objects point to some "bleh" in memory.  
Delegate objects point to some function\(\) in memory.

The "bleh" and function\(\) are immutable, but we can still change what string or function the string/delegate objects point to.

