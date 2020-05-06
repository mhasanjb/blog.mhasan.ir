---
layout: post
comments: true
published: true
title: Angular Multiple Template
categories: angular
---
Creating multiple layout & templates for angular    
With this trick you can have multiple layouts for each component ( home , about , etc )    

1 --> create new project with routing
```
ng new client --skip-tests=true
```

2 - cd client

3 - ng serve

4 --> Generate:Boots
```
ng g c boot/page-content (optional)
ng g c boot/home/home-boot
ng g c boot/blog/blog-boot
```

5 - Add starting app from in boot/page-content/page-content.component.html and app.component.html
```
<router-outlet></router-outlet>
```

6 --> Generate:Contents (for example : we have gold , silver layout)
```
ng g c layout/home/gold/gold-home-footer
ng g c layout/home/silver/silver-home-footer

ng g c layout/blog/gold/gold-blog-footer
ng g c layout/blog/silver/silver-blog-footer
```

7 - Add routing in : app-routing.module.ts
```
import { HomeBootComponent } from "./boot/home/home-boot/home-boot.component"
import { BlogBootComponent } from "./boot/blog/blog-boot/blog-boot.component"

const routes: Routes = [
    {
        path: "",
        component: HomeBootComponent
    },
    {
        path: "Blog",
        component: BlogBootComponent
    },
]
```

8 - Add Controller (data service / condition / etc.) to boot/home/home-boot.component.ts and boot/blog/blog-boot.component.ts
```
export class HomeBootComponent implements OnInit {
    listOfTemplates = ['gold', 'silver']
    template = 'gold'
    condition = this.listOfTemplates.includes(this.template)

    constructor() {}

    ngOnInit() {}
}
```

9 - Add HTML selectors in boot/home , boot/blog

9-1: boot/home/home-boot.component.html
```
<ng-template [ngIf]="template == 'gold'">
    <app-gold-home-footer></app-gold-home-footer>
</ng-template>

<ng-template [ngIf]="template == 'silver'">
    <app-silver-home-footer></app-silver-home-footer>
</ng-template>

<ng-template [ngIf]="!condition">
    <h1>Default</h1>
</ng-template>
```

9-2: boot/blog/blog-boot.component.html
```
<ng-template [ngIf]="template == 'gold'">
    <app-gold-blog-footer></app-gold-blog-footer>
</ng-template>

<ng-template [ngIf]="template == 'silver'">
    <app-silver-blog-footer></app-silver-blog-footer>
</ng-template>

<ng-template [ngIf]="!condition">
    <h1>Default</h1>
</ng-template>
```

10 - End :)

*4 --> Generate:Boots *you can skip page-content and use only app.component.html