# BONSAI Hackathon 2019

### Software methods

---
## Overview

1. SCRUM
2. Test Driven Development
3. On Software Practice

---

<!-- .slide: data-transition="zoom" -->

## Agile mindset
#### [A manifesto](https://agilemanifesto.org/iso/ca/manifesto.html)

+ People over process. Work starts with the people present, they are the right team. Automatization leads to more responsability.
+ It works !

---
### SCRUM

_Living the Agile values in a project_

+ Specification, Architecture, Programming, Testing **IN PARALLEL**
+ Visual management helps communication (post-it walls, boards on github)
+ Roles:
    + Product Owner -> _What needs to be done ? (challenge)_
    + SCRUM master -> _What gets done first ?_
    + Developers -> _Let's build it !_


---
#### DEVOPS

People in the center required less friction in development.

*DEVOPS* is a closer collaboration between development & operations teams

That's when Continuous Integration and Deployment became important

automatic, boring tasks can be done automatically (testing, deploying, upload)

<!-- .slide: data-transition="zoom" -->
---

## Test Driven Development
### Fail first, fail fast
---

### General workflow for TDD

![images](/images/tdd-flow.png)

---

### python basics

+ A test can be a function
+ Tests can be aggregated in suites (groupped in classes)
+ assert that the expected output matches the inputs

---

### simple test in python

If you defined a function called `get_statement` in the 
subpackage "worker" of your `<project_name>`, then you can start with:


```
import pytest
import buyrandom.worker

def test_get_statement():
    # get statement, with a fixed seed 
    # should always return the same contents
    s1 = buyrandom.worker.get_statement(42)
    s2 = buyrandom.worker.get_statement(42)

    assert s1 == s2

```

---

### python testing suggestions

+ `pytest` for starters
+ add a  `tests` directory in your repo
+ before commit, make sure your **code** passes the tests
+ coverage means: _How much of your code is tested ?_

---

## running the tests

```
pytest tests
============================= test session starts =============================
platform linux -- Python 3.6.8, pytest-4.3.0, py-1.8.0, pluggy-0.9.0
rootdir: /home/tomas/workspaces/samurai/buyrandom, inifile: pytest.ini
plugins: cov-2.6.1
collected 2 items                                                                                                                                                                           

tests/test_seedfactory.py .                                                                                                                                                           [ 50%]
tests/test_worker.py .                                                                                                                                                                [100%]

============================= 2 passed in 0.01 seconds ========================
```

---

### code coverage

```bash
pytest --cov=my_project_name tests

----------- coverage: platform linux, python 3.6.8-final-0 -----------
Name                             Stmts   Miss  Cover
----------------------------------------------------
buyrandom/__init__.py                1      0   100%
buyrandom/adjective.py               5      0   100%
buyrandom/bin/__init__.py            0      0   100%
buyrandom/bin/buyrandom_cli.py      23     23     0%
buyrandom/noun.py                    5      0   100%
buyrandom/place.py                   5      0   100%
buyrandom/seedfactory.py            12      0   100%
buyrandom/worker.py                 13      0   100%
----------------------------------------------------
TOTAL                               64     23    64%

```

---

### Minimal pytest HOWTO

1. make sure you have a tests directory (already there if you folloewd the `python-skeleton` format)
2. install `pytest` and `pytest-cov` in your environment

```
conda install -c conda-forge pytest pytest-cov
```
3. run `pytest` in the root directory of your project:

```
pytests --cov=<my_project_name> --cov-report xml:coverage-reports/coverage-<my_project_name>.xml tests

```
This will prepare the test report to be uploaded to sonarqube
Otherwise, for local inspection invoke the command pytest without --cov-report

---
### There is more to know

+ fixtures: _baseline data/objects for tests to be reproducible_
+ specialized packages (Hypothesis - random inputs for tests)
+ Databases ?

---
## Why tests ?

+ Bonsamurai contributes code, before accepting it (using a Pull-Request in gitghub)
    + When her code is merged, make sure it doesn't break anything
+ Guarantee of quality: extreme conditions (testing against negative values, exceptional cases, etc.) are properly handled
+ debugging before the bug bites you ;)
 

---

<!-- .slide: data-transition="zoom" -->

### BONSAI hackathon 2019 tools

1. [`python-skeleton`](https://github.com/BONSAMURAIS/python-skeleton/)
2. coveralls (github integration)
3. travis.org CI (github integration)
4. sonarqube (github integration / local with docker)


---

### standing on the shoulders of giants

Python libraries that already do what you need:

+ appdirs - Store application data
+ docopts - parse options for a cli by documenting them only
+ voluptuous - validate data format
+ pandas - data analytics
+ begins - "forget about if __name__ == 'main? "
+ tqdm - jupyter and cli compatible progress bars
+ flask - quickly deploy a web app
+ connexion - deploy a flask web app, from a OpenAPI 2.0 specification

---

### style and format

+ [opensource libs for pycode](https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code) 
+ pylama (can recall most previous)
