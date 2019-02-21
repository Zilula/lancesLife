---
title: React 101 -- What do you Meme?
date: "2019-02-20"
---


What do you meme?

This past week I dove head first into react. With so much hype around Facebook`s development prodigy, I thought it would be much shinier. But so far that hasn't been the case. Coming from a background in Vue, with single file components being the focus, switching to react where things are broken down by file was a drastic change. Also??? Everything in react is a class? I guess that's a thing. No problems working for classes but I am genuinely curious why that is the case?

There is a lot of division within the react community(from what I can via random people`s very opinionated blog). Half the people really enjoy the class-based components and react provides many ways to use them. You have your standard, functional class component. You have a Pure component and just a normal react class component. And then there is state. Which is an entirely another beast? A very cool and contrary to what I might have said earlier is very shiny. Reach allows you to control data and events from a central location( normally the parent of the situation) and feed new data and event things down the latter to all the children to react(ha) accordingly. 

If in the following bit of blog I`m going to (poorly) explain some basic concepts of React used to make a Meme Generator. 

Alright so first off we have this object called 'state' which as mentioned above is a to store all the different variables and their, well current state. Right now fontColor is default set to white, but there is an option/selector that allows the user to change the color to black. When the change is made,  it fires a function called 'handleChange' which updates the appropriate state key and value. 

![First photo](./2.png)

These state variables are then passed down during binding and prop drilling into child components where that child may then render using the props/data. 


![Second photo](./1.png)

Here we still a component called 'Controls' which contains a form that takes all the various inputs that are needed to generate the meme. Font, captions, color, and URL. All of these have fired that function 'handleChange' as mentioned above to update the parent component in of the change. 
![Third photo](./3.png)

And thats all she wrote folks. See ya next time.