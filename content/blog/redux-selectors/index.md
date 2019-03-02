---
title: React 103 W/redux -- Redux selectors
date: "2019-03-01"
---
Part two of dive into redux we are going to talk about selectors. Fortunately, selectors are incredibly simple. They go to our store and 'select' and return some variables from our store. 
for instance, If you store with some data in it like so.

```
const initialState = {
    notes: [{ title: 'TITLE', body: 'BODY' }, { title: 'TITLE2', body: 'BODY2' }]
};
```
You could write a selector that return the entire array of item like this.

``` 
export const getNotes = state => {
    return state.notes;
};
``` 
This reducer takes the state as a prop and simply returns the array of notes. Simple.

In the next post, I`m gonna introduce reducers and finally, how they all come together. 