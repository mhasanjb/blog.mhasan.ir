---
layout: post
comments: true
published: true
title: angular-multiple-template-simple
categories: angular
---
Simplest way to have multiple template layout for each component in angular
with this your app will look like this : 

```
Home
	Default
    Gold
    Silver
    etc.

Blog
	Default
    Gold
    Silver
    etc.
```

# More explanation
Imagine letting your users to choise a layout, so they will choice a comfortable layout for themself.    
of course you have to create more layouts , but after all it's so good for your users.
( it's like gmail template choesing - modern, simple, etc.  )

# How to use
1 - create project with angular cli
```
ng new multiple-template --routing=true --skipTests=true
```

2 - change directory to the project folder ( multiple-template ) 
```
cd multiple-template
```

3 - create components ( home , blog , about , profile , settings , etc )
```
ng generate component home
```

4 - 


# Requirements 
1 - Install node.js ( download LTS if you are new )
[Download Node.JS From Official Website ](https://nodejs.org/en/download/ "Node.JS")

2 - Install angular/cli
```
npm install -g @angular/cli
```