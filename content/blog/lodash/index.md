---
title: Lodash.
date: "2020-01-26"
---



Figured it was a good time to make a blog posting seeing as I haven't posted in what feels like an entirely even through it been maybe 3? months. Either way. Today I'm going to tell you all about Lodash and why you should be using it. 

Lodash is the predecessor of underscore JS which is essentially a collection of javascript methods. Some have been built into ES6/ES8 things like reduce, map, filter, etc. Common javascript array methods. However, Lodash takes it to another level by applying all these tools to collections/objects. Furthermore, it also has more functions that you will ever need. so I'm gonna list 10 of the most common methods I use every day.

1. Map -- Sometimes you don't need to change something or even have an array so with Lodash's map you can have the best of both worlds
```javascript
const updatedThings = map(someArray, x =>  
        counter += 1;
        return SomeModel.findByIdAndUpdate(x._id, {
          something: something
        });
      })
```

2. Get -- Get is amazing, it allows you too look for the next property in an object and return it or return a safety/default value if it comes up undefined

```javascript
const firstName = get(someObject, 'name.first')
```

3. Filter -- Again, like map filter does the same thing you generally expect it does but does it without having to chain anything

```javascript
const correctPicks = filter(picks, pick => pick && pick.stage === _id);
```

4. Truncate. -- While much less fancy then other Lodash methods, I use truncate often to shorten the length of strings for display purposes. 

```javascript
  const userName = truncate(userObject.firstName { length: 12 });

```

5. Chain -- Okay cool all these methods with Lodash allow you to not chain things together like standard javascript, but what if you need to? well with Chain you can chain all the Lodash methods together like you would in standard javascript. 

```javascript
const sortedPicks = chain(raffleEntries)
      .map(e => ({
        ...e
      }))
      .sortBy('correctPicksNum')
      .reverse()
      .value();
```