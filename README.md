# What Import

## import lib

* `python3 ./what_import/main.py`
```
func was called
```

* `python3 -m unittest`
```
ImportError: Failed to import test module: tests.test_main
  File "what_import/what_import/main.py", line 1, in <module>
    import lib
ModuleNotFoundError: No module named 'lib'
```

## from . import lib

* `python3 ./what_import/main.py`
```
Traceback (most recent call last):
  File "what_import/./what_import/main.py", line 2, in <module>
    from . import lib
ImportError: attempted relative import with no known parent package
```

* `python3 -m unittest`
```
func was called
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```
