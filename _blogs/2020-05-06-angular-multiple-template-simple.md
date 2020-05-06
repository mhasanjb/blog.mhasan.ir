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

# Requirements 
1 - Install node.js ( download LTS if you are new )
[Download Node.JS From Official Website ](https://nodejs.org/en/download/ "Node.JS")

2 - Install angular/cli
```
npm install -g @angular/cli
```