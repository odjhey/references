- most are rephrased from existing concepts that may or may not yet proven/used in production
- most could be general rules, unless context is specified, most are from a nodejs perspective

1. `methodThatCouldError() : {ok: true, data: any} | {ok: false, error: any}` <- this signature is king
   - alternative is the Result type = `type Result<S, E> = Success<S> | Error<E>; type Success<T> = {kind: "", data: T} ; type Error<T> = {kind: "", data: T}` **very important ung `kind`
3. use date as truthy values over plain booleans for flags when storing values (i.e. prefer `publishedAt` over `isPublished`when storing), `isPublished` has still value in predicate functions
4. IoC (what else?) simply throw and interface in the middle. done.
5. `parsing` as a form of validation
6. data flow phases should be obvious (dirty -> clean)
   - freshly received data starts as `dirty`
   - clean it by parsing
   - profit (meaning you dont have to check `if null` if `NaN` etc etc if data is cleaned and reliable
7. only pass what is needed, dont pass the whole data structure, prefer smaller fragments of the whole, only pass what is needed


### todo
- [ ] find better ways of showing/teaching `transducers`
- [ ] checkout select pattern (see mst-gql for selector implementation if necessary)  
```js
useQuery(..., {
  select: someFunctor()
})
```
- [ ] transformation usecases (form <-- --> api, api <-- --> ui) 


## ui
- always require height, width, and aspect-ration, to avoid this thing called Cumulative Layout Shift (CLS)
 https://web.dev/cls/
- read about design tokens
- remote data pattern (cells) -> type RemoteState<E, T> = notAsked(aka initializing) | loading | failure<E> | success<T> , could be used as WebRemote<T> = RemoteState<GQLErr|HttpErr, T>
- restrict components so that only pages has access to (globals) path/url/queries.
