# OS Agnostic file paths

{% tabs %}
{% tab title="New" %}
```python
from pathlib import Path
Path.cwd() # bash pwd
Path.home() # bash HOME directory

bashprofilepath = (Path.home()).joinpath('.bash_profile')
bashprofilepath.is_file()
bashprofilepath.is_dir()

Path.cwd().joinpath('temp').mkdir() #make directory
Path.cwd().joinpath('temp').rmdir() #remove directory

somedir = (Path.home()).joinpath('folder')

#We can iterate files of a directory using its path
for fileX in somedir.iterdir():
    print(fileX.name)
```
{% endtab %}

{% tab title="Python" %}
```python
import os
os.getcwd() #print current directory, pwd in bash
os.chdir("somefolder") #change directory, cd in bash
os.path.abspath("./somefolder") #print out absolute path

os.path.join(os.getcwd(),"somefolder") #/home/user/somefolder or C:/User/somefolder
# OS agnostic joining paths

os.listdir(".") #list files, ls .
os.path.isdir("heh") #checks heh is a folder
os.path.isfile("heh") #check heh is a file

```
{% endtab %}
{% endtabs %}

```python

```

