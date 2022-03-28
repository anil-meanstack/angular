# what is data binding?
Data binding is the core concept of angular application. Data binding means communication between your code and template files. e.g we assign any value to the variable and output value into the template file.

# types of data binding
1.Interpolation

2.String Interpolation

3.Property Binding

4.Event Binding

5.Two-way binding

# Interpolation
value print {{variable}}

# string interpolation

``` 
export class appcomponent {
     
     name: string ="anil";
     
    }
 ```
  
# property binding    

```
img[src]="img path";

```
# event binding
app.component.html file

```
button (click)="onSave()">Save</button>
```

app.component.ts file

```
onsave(){ alert("yes");}
```

# two-way binding
 import Forms module in app.module.ts file.
 
 # all component call in declarations
  
``` 

   declarations:[
               AppComponent,
               
               ContactComponent,
               
               AboutComponent,
               
               ShopComponent,
               
               NavComponent,  
  ]
 ```
```
import {FormsModule} from '@angular/forms';

all module call in imports[]

imports:[
         FormsModule
      ]
```

```

export class appcomponent{
     
     name: string ="anil";
     
    }
 ```
 
 app.component.html file
 
 ```
 <input [(ngModel)]="name">
 
 {{name}}
 
 ```
# Add nevigation with routing
```
 <a routerLink="/contect" routerLinkActive="active">Contect</a> 
 ```
 
 # sturcture directives
 ***ng if*** 
 
***ng if-else***

***ng for***

# ng if

***ng if used for hide show in html***

```
component.html file

<p *ngIf="name" >this is coming from contact page!</p>

<button (click)="showHide()" >Toggle</button>


component.ts file

 constructor() { 
  
  name = false;
  
    showHide(){

    if(this.name == true)
    {
      this.name = false;
    }else{
      this.name = true;
    }

}

```

# ng for
***component.html file***

```
<div *ngFor="let name of data" >
    <P>{{name}}</P>
</div>
<input type="text" [(ngModel)]="stuName" >

<button (click)="addName()" >Add name</button>
<button (click)="rName()" >Remove name</button>

```

***component.ts file***

```
addName(){
    
    this.data.push(this.stuName)
    this.stuName="";
  
  }
  
  rName(){
    //this.data.pop(this.stuName)
        var index = this.data.indexOf(this.stuName);
      if (index !== -1) {
        this.data.splice(index, 1);
      }
  }
```





