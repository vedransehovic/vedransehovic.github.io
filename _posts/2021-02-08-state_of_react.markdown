---
layout: post
title:      "State of React"
date:       2021-02-08 18:47:41 +0000
permalink:  state_of_react
---


Recently I've spent couple of months learning the basics and intricacies of React. React is, for those who are not aware, JS front end framework developed by Facebook in 2011. Since then it gained enourmous popularity and is now of the the most popular web front ends out there. 

When I first started using it it made a lot of sense, it streamlined the whole process, JSX was godsend and components made everything easier to follow and code. However, soon after, cracks begun to show. Passing state through props was easier one or two levels down but after that it became nightmarish. Not to speak of passing anything back upstream. 

Knowing that we are going to go over Redux in our curriculum I wasn't worried too much. I knew what Redux is and how it deals with the state and was happy to embrace it. Redux is essentially a library that makes the React state global and every component can just connect to it. Well that's the idea anyway and it sounds great. However putting it in practice is cumbersome, and hard, wiring everything up, state, actions, reducers, dispatch and making it all work is an absolute nightmare for a beginner. Even after working on a project with React / Redux I feel I'm not much better with it. It's just cumbersome and I'm avoiding it every chance I get. It shouldn't be that way. 

Global state should exist, don't get me wrong, it's a fantastic idea but Redux implementation is cumbersome and archaic and should change to something else. It would be amazing that it's part of React by default, containing few hooks, ways to dispatch and get state. It would be great to have it React native, usable right out of the box. 

So, who is working on it?
