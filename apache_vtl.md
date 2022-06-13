# Apache Velocity Template Language

Doc: [here](https://velocity.apache.org/engine/1.7/user-guide.html)

- All statements begin with a `#`
- All statements contain a directive

- `References` begin with `$` and are used to declare variables and retrieve their values later
- `Directives` begin with `#` and are used to do something

## References

1. Variables
  - `$` sign in front of them
  - created with a `#set` directive

### Utility Functions

- `$util.qr` === `$util.quiet` can be used to call methods

### Loops

```

#set($range = [$start..$end])

#foreach($loop_variable in $iterable)
  ...
#end
```

### Conditionals

```
#if(condition)

#else / #elseif

#end
```

## Context

- `map` that holds all contextual information for your resolver invocation

```js
{
   "arguments" : { ... },     // all graphql arguments
   "source" : { ... },        // resolution of parent field
   "result" : { ... },        // container for the results of this resolver, available only to response mapping templates.
   "identity" : { ... },      // information about the caller
   "request" : { ... },
   "info": { ... }
}
```

- `stash` is a map made available inside each resolver and function mapping template. Same stash instance lives through a single resolver execution.

## Util

- `$util.toJson($object)`
- `$util.parseJson($string)`
- `$util.unauthorized()`
