- most are mine, and may or may not yet proven/used in production
- most could be general rules, unless context is specified, most are from a nodejs perspective

1. `methodThatCouldError() : {ok: true, data: any} | {ok: false, error: any}` <- this signature is king
2. use date as truthy values over plain booleans for flags when storing values (i.e. prefer `publishedAt` over `isPublished`when storing), `isPublished` has still value in predicate functions
3. IoC (what else?) simply throw and interface in the middle. done.
4. `parsing` as a form of validation
5. data flow phases should be obvious (dirty -> clean)
   - freshly received data starts as `dirty`
   - clean it by parsing
   - profit (meaning you dont have to check `if null` if `NaN` etc etc if data is cleaned and reliable
6. only pass what is needed, dont pass the whole data structure, prefer smaller fragments of the whole, only pass what is needed


### todo
- [ ] find better ways of showing/teaching `transducers`
