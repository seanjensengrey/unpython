unPython is a Python to C compiler. unPython compiles a type-annotated subset of Python to C code.Type annotations are added through decorators or as strings discarded by the Python interpreter. Thus your annotated source is still 100% pure python and will run unmodified on the interpreter. unPython also aims to be numpy aware i.e. be able to compile numpy constructs.


# About #

unPython was originally developed at as part of a research project at the Systems Lab, Dept of Computing Science, University of Alberta by me (Rahul Garg) under the supervision of [Prof Amaral](http://www.cs.ualberta.ca/~amaral/) for my MS Thesis. I have graduated and now continuing to work on unPython

# Update #

A considerably rewritten version is scheduled to be released in December 2010 and includes GPU support. An academic version can be found at [this DOI](http://dx.doi.org/10.1145/1735688.1735695)

# Example #
```
@unpython.type('int','int','int')
def f(x,y):
    #type of temp is inferred by compiler to be 'int'
    temp = x+y 
    return temp

```

# Feedback #
As an open source project, community feedback is very very important. If you had problems in downloading or running the compiler do let me know. You can file bugs on this site. You can also contact or report problems through the mailing list (look at the right side-bar for link) or directly emailing whycode at the domain gmail.com. I guarantee a fast response to bug reports, comments, feature requests, flames.
