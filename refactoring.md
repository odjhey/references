### Conditionals
reason why we do conditions, 
1. preconditions, aka guards
2. many ways to compute something, `x ? compute(x) : compute(1)`

above cases are better expressed differently, like for (1), use a guard clause, and for (2) an interface/ternary/or regular if/else

### abstractions should happen during refactor phase and not before.
### code reuse is not the end-goal, extract to reduce code, do not extract to reuse. their is a thin line between the two.

### fix some TODO/FIXME tags when encountered, we leave these to be done at a later time and this time may be that time, if your intended change is part of the TODO/FISME note/comment, please take some time to address em too. thanks

### small refactors diff friendly, diff friendly PRs will almost always be approved for merge.
