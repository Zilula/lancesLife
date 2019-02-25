---
title: React 102 -- Lifting state up
date: "2019-02-25"
---


React state more or less has two main stages. Local state and what I`m going to refer to as global state. Local state is as it sounds. The state of a component relative to itself. Meaning the changes that happen in or through a component never leave or have an impact on other components. Any changes to data only update the properties within the single component. 

On the other end, we have global state. Which is a little vaguer as in this case global isn't being used in the same manner as say a global npm package. In my usage, global refers to a single point of 'truth'. Aka a parent component who actually owns the state for several child based components. React state can be passed down to children through binding/prop drilling and lifted back up by calling methods on the parent component that updates that single origin of 'truth' Aka the parent`s state. 

At this point is also probably important to note that you can more than one point of origin for state. It should really depend on the scope of the project and from there you can determine who needs to have access to certain properties.

Per the react documentation, using a single point of truth 'greatly reduces surface area' of bugs and potential problems. So in theory, because everything originates from a single point, it is easier to track down bugs and issues. 

Its very much worth checking out the react documents on lifting state up. 
https://reactjs.org/docs/lifting-state-up.html 