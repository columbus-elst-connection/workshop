# Command Line Interface

The entrypoint to our program is a good place to start, so that we can get a
sense for how all the pieces will fit together. The interface we're looking for
is something like this: 

```plain
l-system -f <l-system-file> -n <iterations>
```

We need a few main pieces in order to render an l-system. First is a file
containing the description of our l-system. This will have the rules for symbol
replacements, defines the _axiom_ and it will also contain some starting
configuration for our renderer. 
Lastly we have the number of iterations, which is the number of times that we
should apply the token substitution rules.

The `main` function should parse these arguments, parse the l-system described
in the file, then get the final productions and pass them to the renderer as
individual instructions. Once that is complete, it should call finalize on the
renderer. 
