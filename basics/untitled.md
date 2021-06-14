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

