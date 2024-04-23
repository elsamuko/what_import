# What Import

## `import lib`

* `python3 ./what_import/main.py`
```bash
func was called
```

* `python3 -m unittest`
```bash
ImportError: Failed to import test module: tests.test_main
  File "what_import/what_import/main.py", line 1, in <module>
    import lib
ModuleNotFoundError: No module named 'lib'
```

## `from . import lib`

* `python3 ./what_import/main.py`
```bash
Traceback (most recent call last):
  File "what_import/./what_import/main.py", line 2, in <module>
    from . import lib
ImportError: attempted relative import with no known parent package
```

* `python3 -m unittest`
```bash
func was called
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```

## `from what_import import lib`

* `python3 ./what_import/main.py`
```bash
Traceback (most recent call last):
  File "what_import/what_import/main.py", line 3, in <module>
    from what_import import lib
ModuleNotFoundError: No module named 'what_import'
```

* `python3 -m unittest`
```bash
func was called
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```
