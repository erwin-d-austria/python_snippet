Author: e.d.austria
Date: 11/27/18
Version: 1.0
Link:(https://github.com/erwin-d-austria/python_snippet)

# How to setup Virtual Environment using virtualenv

**virtualevn** is used to manage Python packages for different projects. Using virtualenv allows you to avoid installing Python packages globally which could break systems tools or other projects.

**This is for windows only!**

Installing:
``` python
pip install virtualenv
```
Creating:
``` python
virtualenv -p 'version of python you want to use' 'name of env'
virtualenv -p C:\Users\e.d.austria\AppData\Local\Programs\Python\Python35\python.exe env3.5
```
Activating:
```python
.\'envName'\Scripts\activate
.\env3.5\Scripts\activate
```
Leaving the virtualenv
```python
deactivate
```