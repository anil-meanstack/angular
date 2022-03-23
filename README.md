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
 
```
import {FormsModule} from '@angular/forms';
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
