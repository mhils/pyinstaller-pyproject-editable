# PyInstaller + editable `pyproject.toml` installs

**Working:**

```
$ pip install .
$ pyinstaller --clean --onefile bin/repro.py
$ dist/repro
hello world
```

**Crash:**

```
$ pip install -e .
$ pyinstaller --clean --onefile bin/repro.py
$ dist/repro
Traceback (most recent call last):
  File "repro.py", line 1, in <module>
ModuleNotFoundError: No module named 'my_module'
[2041] Failed to execute script 'repro' due to unhandled exception!
```
