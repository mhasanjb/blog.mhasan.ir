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

or

ng g c home
ng g c about
ng g c profile
```

4 - go to src/app/home/home.component.html
```html
<!-- Gold Layout -->
<div *ngIf="template == 'gold'">
    <!-- Your HTML code here for gold layout -->
    <h1>Gold layout</h1>
    <p>This is gold layout</p>
</div>


<!-- Silver Layout -->
<div *ngIf="template == 'silver'">
    <!-- Your HTML code here for silver layout -->
    <h1>Silver layout</h1>
    <p>This is silver layout</p>
</div>


<!-- More layouts here -->
<!-- ... -->
```

5 - go to src/app/home/home.component.ts
```typescript
import { Component, OnInit } from '@angular/core';
// add your service here for getting user data (like template , etc.)

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.css']
})
export class HomeComponent implements OnInit {
  
  template = 'gold' // you have to get this user's data with service from backend

  constructor() { }

  ngOnInit(): void {}

}
```

6 - go to src/app/app-routing.module.ts
```typescript
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { HomeComponent } from "./home/home.component"


const routes: Routes = [
  {
      path: "home", // you can also make it / ,then your home components will open in root (localhost:4200) 
      component: HomeComponent
  },
]

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

7 - go to src/app/app.component.html and remove every thing and copy/paste this code:
```html
<router-outlet></router-outlet>
```

8 - ng serve ( and wait for angular to make everything ready )

9 - go to -> localhost:4200/home

10 - that's it :)

this is minimalest way to create multiple layout in angular, if you need 

# Requirements 
1 - Install node.js ( download LTS if you are new )
[Download Node.JS From Official Website ](https://nodejs.org/en/download/ "Node.JS")

2 - Install angular/cli
```
npm install -g @angular/cli
```