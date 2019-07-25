
# File build\_doc.py

[**File List**](files.md) **>** [**build\_doc.py**](build__doc_8py.md)

[Go to the documentation of this file.](build__doc_8py.md) 


````cpp
# The Script : https://gist.github.com/an-dr/9f3256f4ccd97bc6e04751b542364bff

from os.path import realpath, dirname, join
from os import system as x


def x(cmd):
    # imports
    from psutil import MACOS, WINDOWS, LINUX
    from subprocess import Popen as shell
    from sys import stdout
    # shell cfg
    if WINDOWS:
        SHELL, NEXT_CMD = "powershell", ";"
    elif MACOS or LINUX:
        SHELL, NEXT_CMD = "sh", ";"
    # run
    shell([SHELL, NEXT_CMD.join(cmd)], stdout=stdout).communicate()


THIS = dirname(realpath(__file__))


X = [
    "cd %s/../.." % THIS,
    "pushd ./docs/src",
    "doxygen",
    "popd",
    "doxybook -i ./docs/src/doxygen/xml/ -o ./docs/generated -t mkdocs"
]
x(X)
````

