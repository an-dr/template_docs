
# Namespace build\_doc


[**Class List**](annotated.md) **>** [**build\_doc**](namespacebuild__doc.md)


















## Public Attributes

| Type | Name |
| ---: | :--- |
|   | [**THIS**](namespacebuild__doc.md#variable-this)   = =  dirname(realpath(\_\_file\_\_))<br> |
|  list | [**X**](namespacebuild__doc.md#variable-x)   = =  [
    "cd %s/../.." % THIS,
    "pushd ./docs/src",
    "doxygen",
    "popd",
    "doxybook -i ./docs/src/doxygen/xml/ -o ./docs/generated -t mkdocs"
]<br> |


## Public Functions

| Type | Name |
| ---: | :--- |
|  def | [**x**](namespacebuild__doc.md#function-x) (cmd cmd) <br> |








## Public Attributes Documentation


### variable THIS 


```cpp
build_doc.THIS;
```



### variable X 


```cpp
list build_doc.X;
```


## Public Functions Documentation


### function x 


```cpp
def build_doc::x (
    cmd cmd
) 
```



------------------------------
The documentation for this class was generated from the following file `build_doc.py`