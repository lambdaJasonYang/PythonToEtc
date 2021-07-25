# Dev environment

{% tabs %}
{% tab title="Haskell" %}
```haskell
stack ghci test.hs
```
{% endtab %}

{% tab title="C++" %}
```
g++ myfile.cpp
./a.out
```
{% endtab %}

{% tab title="C\#" %}
```
cd [directory that contains Program.cs]
dotnet run Program.cs
```
{% endtab %}
{% endtabs %}

```text
stack ghc --package QuickCheck -- main.h
```



task.json in the ".vscode" folder holds the task that runs the files. Modifying the task.json tips use ${file} to get current file

The tasks you can run depends on where you "Opened" vscode. eg. if you opened the parent folder of the haskell folder, you will get only the parent tasks, not the haskell tasks.

Ctrl+P then type "task" then space Or click Run Task...

GIT, download a repo or subfolder in a repo "cd someFolder" "git clone [https://github.com/fullstack-hy2020/part3-notes-backend.git](https://github.com/fullstack-hy2020/part3-notes-backend.git)"

