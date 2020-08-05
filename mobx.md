# MobX Notes

### unordered _aha's_

- observable applies itself recursively by default, so all fields in an observed object are observables
- `getDependencyTree(disposer)` logs the dependencytree of the disposer (i.e. reaction or autorun)

### autorun

- `autorun(( ) => { ... })`
- triggered once immediately
- triggered each time one of its dependencies change
- use autorun if a function should run automatically but does not result in a new value
- autorun is about initiating effects
- returns a disposer function for cleanup

### reaction

- `reaction(() => { return **dependencies** }, (**dependencies**) => { ... })`
- a variation on autorun
- 'a reaction requires you to produce the things (data) you need in your side effect (effect)'
- the effect **only** reacts to data that is specifically returned in the data function!
- takes two functions
  1. the data function declares the dependencies to observe by returning them
  2. the effect function is triggered when dependencies change and is passed
     - the updated values/dependencies
     - the reaction itself, for a possible cleanup during execution
- returns a disposer function for cleanup
