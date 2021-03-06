# Shapes Cython-C++ Examples

### Purpose
Simple examples for Cython C++ API from [Using C++ in Cython](http://docs.cython.org/src/userguide/wrapping_CPlusPlus.html). The website doesn't illustrate the complete program. This leads to difficulty understanding the placement of information in files. The shapes example remedies those problems.

### Compilation
To compile code, change directory to folder containing setup.py and type the following at command prompt:
```
python setup.py build_ext --inplace
```

### Example
```
import rect
myRect = rect.PyRectangle(1,2,3,4)
myRect.getArea()
```

### Known Caveats (Subject to Change)

C++ functions external to any class **must** be included in separate .pyx file and wrapped in a pure Python function to be called from Python.
