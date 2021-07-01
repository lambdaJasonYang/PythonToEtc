# OS Agnostic file paths

```python
import os
os.getcwd() #print current directory, pwd in bash
os.chdir("somefolder") #change directory, cd in bash
os.path.abspath("./somefolder") #print out absolute path

os.path.join(os.getcwd(),"somefolder") #/home/user/somefolder or C:/User/somefolder
# OS agnostic joining paths




```

```python
os.listdir(".") #list files, ls .
os.path.isdir("heh") #checks heh is a folder
os.path.isfile("heh") #check heh is a file
```

