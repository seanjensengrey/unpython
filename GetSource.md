# How to get source #

Source is hosted on launchpad in a bazaar repository.
You can get source through :
```
bzr branch lp:unpython
```

# Building #

To build the source, you will need to install ant, scala and also download antlr v3. Ensure that "scalac" is in your path and that antlr jar is in the classpath.

After which you can issue the command "ant" to build a jar or "ant zip" to build the distribution.