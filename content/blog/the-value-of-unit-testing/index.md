---
title: React 104 -- The value of unit testing.
date: "2019-03-08"
---


The power of unit testing cannot be minimized especially by someone in my position. 

I was working on a react /redux application that use a few reducers and a handful of actions/selectors to create a mock blog pulling in data from an API that holds of a bunch of fake blog like data. 

Moral of the story is that I wrote this selector that would return an array of blog posts that match filter criteria. I wrote the whole selector which isn't all that much (5-7 lines of code) but I could not for the life of me get my selector to return what I was expecting/wanted. 

SOOOOOO, I broke out the unit testing(shameful, I know) that I should have been using the whole time. Using Jest allowed me to incrementally test what I was getting back at each step of the filter function. 

Was I getting the search term back from the redux/state?
Was I getting an array of posts to filter by in the first place?
I wasn't. At each point what I thought I was doing, was not what was actually happening. Turns out I could not set a variable equal to what gets returned from an API because the function would use the variable before the variable contains any actual data. 
For reference, this is what the final function looks like. 

``` 
export const getPostsBySearch = (state) => {
  const searchTerm = getSearchTerm(state);
  const filtered = getPosts(state).filter(post => {
    const { title } = post;
    return title.includes(searchTerm);

  });
  return filtered;
} 
```

Originally I was trying to set  ``` getPosts(state)``` equal to a variable like 'posts'
and call the function like...
 ``` 
export const getPostsBySearch = (state) => {
    const searchTerm = getSearchTerm(state);
    const posts = getPosts(state)
    const filtered = posts.filter(post => {
        const { title } = post;
        return title.includes(searchTerm);
    });
    return filtered;
} 
```

But you can`t do that because posts return a promise to be resolved at a later date. So if I wanted to go down the route I would need to render the remaining part of the function in a then block or use a promise.resolve or some sort of async-await. 

Using the test below I could visibly see that my original function was not doing the things. Or even part of the things. 

``` 
it('returns a filtered array of posts', () => {
    const state = {
        posts: {
        posts: [
            { title: 'sometitle' },
            { title: 'fghfghfgh' }
        ],
        searchTerm: 's'
        }
    }; 
    const results = getPostsBySearch(state);
    expect(results).toHaveLength(1);
});
```

Moral of the story. Write your tests first. 
