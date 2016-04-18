# a2_wp_rxjs-savkin
* clone starter 5.0.4 17/04/16 2.0.0-beta.15
* add Savkin component according [Managing State in Angular 2 Applications by Victor Savkin](http://victorsavkin.com/post/137821436516/managing-state-in-angular-2-applications)

---

* create component Savkin, routing included

app/savkin/savkin.component.ts
<pre><code>
    
    import {Component} from 'angular2/core';  
    
    @Component({
        selector: 'savkin',
        template: require('savkin.html')
    })
    export class Savkin {}
</pre></code>
app/savkin/savkin.html
<pre><code>

    <div>
        <h1>Savkin-State</h1>
    </div>
</pre></code>
app/savkin/index.ts
<pre><code>
export * from './savkin.component';
</pre></code>
app/app.component.ts
<pre><code>

    import {Savkin} from './savkin';
    ...
    |
    <li router-active>
        <a [routerLink]=" ['Savkin'] ">Savkin</a>
    </li>
    ...
    ,
    {path: '/savkin', name: 'Savkin", component: Savkin}
            
</pre></code>
...
