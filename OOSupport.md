# Introduction #

unPython supports compilation of user defined classes to C.
However currently only a subset of Python OO features are supported.
  * Only single inheritance is supported.
  * Each user defined class must have exactly one base class.
  * Properties, classmethods, staticmethods, metaclasses, magic methods (those beginning with two underscores except init) are not supported
  * User defined classes cannot inherit from list, dict, int, long, float, set, tuple or ndarray.
  * Old style classes are not supported. Each class must either inherit from object or from a user defined class which inherits from object.
  * If A is base class of B and A is not "object", then A must be in the same module and A must be statically typed.