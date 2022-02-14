# Angular Interview Questions & Answers
--------

### Table of Contents

| No. | Questions |
|---- | ---------
|1  | [Hoisting?](#hoisting)|
|2  | [Closure?](#closure)|
|3  | [Ngrx?](#ngrx)|
|4  | [Cloning Arrays](#cloning-arrays)|
|5  | [Cloning Objects](#cloning-objects)|
|6  | [ES6 Features](#es6-features)|
|7  | [Combine scripts in angular.json](#combine-scripts-in-angular.json)|
|8  | [Life cycle hooks?](#life-cycle-hooks)|
|9  | [Bootstrapping?](#bootstrapping)|
|10 | [Authguard?](#authguard)|
|11 | [MergeMap?](#mergemap)|
|12 | [SwitchMap?](#switchmap)|
|13 | [Map, Reduce and Filter?](#map-reduce-and-filter)|
|14 | [View Encapsulation?](#view-encapsulation)|
|15 | [Async await and Promise?](#async-await-and-promise)|
|16 | [Sharing data between Components?](#sharing-data-between-components)|
|17 | [Directives](#directives)|
|18 | [Lazy loading](#lazy-loading)|
|19 | [Observable vs Promises](#observable-vs-promises)|
|20 | [How to upgrade angular version](#how-to-upgrade-angular-version)|
|21 | [How you can apply color to the table rows based on the their status(either true/false) with css](#how-you-can-apply-color-to-the-table-rows-based-on-the-their-status(either-true/false)-with-css)|
|22 | [JIT and AOT](#jit-and-aot)|
|23 | [Observable](#observable)|
|23 | [Memory leak](#memory-leak)|



--------
1. ### Hoisting
    Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution

    ```
    function hoist() {
        a = 20;
        var b = 100;
    }
    
    hoist();
    console.log(a); 	// it will print a value as 20
    console.log(b); 	// it will make an error as ReferenceError, where b is local to hoist
    ```
    **[⬆ Back to Top](#table-of-contents)**

2. ### Closure
    A closure is the combination of a function enclosed with references to its surrounding state . In other words, a closure gives you access to an outer function's scope from an inner function
    **[⬆ Back to Top](#table-of-contents)**

3. ### Ngrx
    NgRx is a framework for building reactive applications in Angular. NgRx is inspired by the Redux pattern - unifying the events in your application and deriving state using RxJS. At a high level, NgRx stores a single state and uses actions to express state changes<br >	
	NgRx is made up of 5 main components - Store, Actions, Reducers, Selectors, and Effects

    1. **Store:** You can think of this as a client-side database. The Store in NgRx acts as the application's single source of truth. It reflects the current state of the app
    2. **Actions:** Actions express unique events that happen in our application. These events range from application lifecycle events, user interactions, to network requests. Actions are how the application communicates with NgRx to tell it what to do
    3. **Reducers:** Reducers are responsible for handling transitions between states. Reducers react to the Actions dispatched and executes a pure function to update the Store. Pure functions are functions that are predictable and have no side effects. Given the same set of inputs, a pure function will always return the same set of outputs
    4. **Selectors:** Selectors are pure functions for getting slices of the state from the Store. Selectors are how our application can listen to state changes
    5. **Effects:** Effects handle the side effects of each Action. These side effects range from communicating with an external API via HTTP when a certain Action is dispatched to dispatching another Action to update another part of the State
    **[⬆ Back to Top](#table-of-contents)**

4. ### Cloning Arrays
    3 types to copy an array with out reference.

    ```
    var a = [1,2,3];

    var b = [ ...a ];		//	Spread syntax (...)
    var c = Array.from(a);
    var d = a.slice();
    ```
    **[⬆ Back to Top](#table-of-contents)**

5. ### Cloning Objects
    2 types to copy object without reference.

    ```
    var a = { id:"1", text: "ABC" };

    var b = { ...a };
    var c = JSON.parse(JSON.stringify(a));
    ```
    **[⬆ Back to Top](#table-of-contents)**

6. ### ES6 Features
    1. let and const keywords
	2. Arrow Functions
	3. Multi-line Strings
	4. Default Parameters
	5. Template Literals
	6. Destructuring Assignment
	7. Enhanced Object Literals
	8. Promises
	9. Classes
	10. Modules
    **[⬆ Back to Top](#table-of-contents)**

7. ### Combine scripts in angular.json
    Using && operator we can combine the scripts
	
    #### angular.json
    ```
    "scripts": {
        "devbuild": "ng build --configuration dev --prod && firebase use devtotmaster && firebase deploy",
        "testbuild": "ng build --configuration test --prod && firebase use testtotmaster && firebase deploy"
    }
    ```
	
    #### run command
	```
    npm run devbuild
		or
	npm run testbuild
    ```
    **[⬆ Back to Top](#table-of-contents)**

8. ### Life cycle hooks
    Angular application goes through an entire set of processes or has a lifecycle right from its initiation to the end of the application. The representation of lifecycle in pictorial representation as follows

    1. **constructor**
    2. **ngOnChanges:** When the value of a data bound property changes, then this method is called
    3. **ngOnInit:** This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens
    4. **ngDoCheck:** This is for the detection and to act on changes that Angular can't or won't detect on its own
    5. **ngAfterContentInit:** This is called in response after Angular projects external content into the component's view
    6. **ngAfterContentChecked:** This is called in response after Angular checks the content projected into the component
    7. **ngAfterViewInit:** This is called in response after Angular initializes the component's views and child views
    8. **ngAfterViewChecked:** This is called in response after Angular checks the component's views and child views
    9. **ngOnDestroy:** This is the cleanup phase just before Angular destroys the directive/component
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    Every application has at least one Angular module, the root module that you bootstrap to launch the application is called as bootstrapping module. It is commonly known as AppModule. The default structure of AppModule generated by AngularCLI would be as follows

    ```
    import { AppComponent } from './app.component';
	@NgModule({
	  declarations: [
		AppComponent
	  ],
	  imports: [
		BrowserModule,
		FormsModule,
		HttpClientModule
	  ],
	  providers: [],
	  bootstrap: [AppComponent]
	})
    ```
    **[⬆ Back to Top](#table-of-contents)**

10. ### Authguard
    AuthGuard is a class which implements the interface CanActivate , to decide whether the user has access/permission to view specific page / route / path in the application or not. This will be useful when we need authentication/authorization based control over the application<br >

    **auth.guards.ts::**
    ```
    import { Injectable } from "@angular/core";
    import { ActivatedRouteSnapshot, CanActivate, Router, RouterStateSnapshot, UrlTree} from "@angular/router";
    import { AuthService } from "./auth.service";
    @Injectable()
    export class AuthGuard implements CanActivate {
        constructor(
            private authService: AuthService,
            private router: Router) { }
        canActivate(
            route: ActivatedRouteSnapshot,
            state: RouterStateSnapshot): boolean | Promise<boolean> {
            var isAuthenticated = this.authService.getAuthStatus();
            if (!isAuthenticated) {
                this.router.navigate(['/login']);
            }
            return isAuthenticated;
        }
    }
    ```

    **app-routing.module.ts::**
    ```
    import { AuthGuard } from './services/auth.guards';
    const routes: Routes = [
        { path: '',   component: PostListComponent },
        { path: 'create',   component: PostCreateComponent,   canActivate: [AuthGuard]},
        { path: 'edit',   component: PostCreateComponent,   canActivate: [AuthGuard] },
        { path: 'login',   component: LoginComponent },
        { path: 'signup',   component: SignupComponent }
    ];
    
    @NgModule({
        imports: [RouterModule.forRoot(routes)],
        exports: [RouterModule],
        providers: [AuthGuard]
    })
    ```
    **[⬆ Back to Top](#table-of-contents)**

11. ### MergeMap
    The Angular MergeMap maps each value from the source observable into an inner observable, subscribes to it, and then starts emitting the values from it replacing the original value. It creates a new inner observable for every value it receives from the Source
    **[⬆ Back to Top](#table-of-contents)**

12. ### SwitchMap
    The Angular SwitchMap maps each value from the source observable into an inner observable, subscribes to it, and then starts emitting the values from it. It creates a new inner observable for every value it receives from the Source
    **[⬆ Back to Top](#table-of-contents)**
    
13. ### Map Reduce and Filter

    1. **Map:**
        Map operator takes an observable source as input. It applies a project function to each of the values emitted by the source observable and transforms it into a new value. It then emits the new value to the subscribers

        ```
        import { map } from 'rxjs/operators'

        srcArray = from([1, 2, 3, 4]);

        multiplyBy2() {
            this.srcArray
            .pipe(map(val => { return val * 2}))
            .subscribe(val => { console.log(val)})
        }
        
        ```
    2. **Reduce:**
        The reduce() method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array

        ```
        const numbers = [1, 2, 3, 4];
        const sum = numbers.reduce(function (result, item) {
            return result + item;
        }, 0);

        console.log(sum); // 10
        ```

    3. **Filter:**
        The filter() method takes each element in an array and it applies a conditional statement against it. If this conditional returns true, the element gets pushed to the output array. If the condition returns false, the element does not get pushed to the output array

        ```
        const numbers = [1, 2, 3, 4];
        const evens = numbers.filter(item => item % 2 === 0);
        console.log(evens); // [2, 4]
        ```
    
    **[⬆ Back to Top](#table-of-contents)**

14. ### View Encapsulation
    In Angular, a component's styles can be encapsulated within the component's host element so that they don't affect the rest of the application.<br >

    1. **ViewEncapsulation.ShadowDom:** Angular uses the browser's built-in Shadow DOM API to enclose the component's view inside a ShadowRoot (used as the component's host element) and apply the provided styles in an isolated manner
    2. **ViewEncapsulation.Emulated:** Angular modifies the component's CSS selectors so that they are only applied to the component's view and do not affect other elements in the application (emulating Shadow DOM behavior).
    3. **ViewEncapsulation.None:** Angular does not apply any sort of view encapsulation meaning that any styles specified for the component are actually globally applied and can affect any HTML element present within the application. This mode is essentially the same as including the styles into the HTML itself

    ```
    @Component({
        selector: 'app-encapsulation',
        template: ``,
        styles: [],
        encapsulation: ViewEncapsulation.Emulated, 
        //encapsulation: ViewEncapsulation.None, 
        //encapsulation: ViewEncapsulation.ShadowDom,
    })
    ```

    **[⬆ Back to Top](#table-of-contents)**

15. ### Async await and Promise
    1. **Async-Await:** When an async function is called, it returns a Promise. When the async function returns a value, the Promise will be resolved with the returned value. When the async function throws an exception or some value, the Promise will be rejected with the thrown value
    ```
    async getPrice(currency: string): Promise<any> { 
        return this.httpClient.get<any>("API URL").toPromise(); 
    } 

    this.price = await this.getPrice(this.currency); 
    ```

    2. **Promise:**
    
    #### Syntax:
    ```
    var promise = new Promise((resolve, reject) => {
    });
    ```

    #### Ex:
    ```
    var promise = new Promise((resolve, reject) => {
    setTimeout(() => {
            console.log("Async Work Complete");
            resolve();
        }, 1000);
    });
    ```
    **[⬆ Back to Top](#table-of-contents)**

16. ### Sharing data between Components
    There are five ways to share data between components
    1. **Parent to Child: Sharing Data via Input**
        This is probably the most common and straightforward method of sharing data. It works by using the @Input() decorator to allow data to be passed via the template

        ##### parent.component.ts
        ```
        import { Component } from '@angular/core';
        @Component({
            selector: 'app-parent',
            template: `
                <app-child [childMessage]="parentMessage"></app-child>
            `,
            styleUrls: ['./parent.component.css']
        })
        export class ParentComponent{
            parentMessage = "message from parent"
            constructor() { }
        }
        ```

        #### child.component.ts
        ```
        import { Component, Input } from '@angular/core';
        @Component({
            selector: 'app-child',
            template: `
                Say {{ message }}
            `,
            styleUrls: ['./child.component.css']
        })
        export class ChildComponent {
            @Input() childMessage: string;
            constructor() { }
        }
        ```

    2. **Child to Parent: Sharing Data via ViewChild**
        ViewChild allows a one component to be injected into another, giving the parent access to its attributes and functions. One caveat, however, is that child won’t be available until after the view has been initialized. This means we need to implement the AfterViewInit lifecycle hook to receive the data from the child

        #### parent.component.ts
        ```
        import { Component, ViewChild, AfterViewInit } from '@angular/core';
        import { ChildComponent } from "../child/child.component";
        @Component({
            selector: 'app-parent',
            template: `
                Message: {{ message }}
                <app-child></app-child>
            `,
            styleUrls: ['./parent.component.css']
        })
        export class ParentComponent implements AfterViewInit {
            @ViewChild(ChildComponent) child;
            constructor() { }
            message:string;
            ngAfterViewInit() {
                this.message = this.child.message
            }
        }
        ```

        #### child.component.ts
        ```
        import { Component} from '@angular/core';
        @Component({
            selector: 'app-child',
            template: `
            `,
            styleUrls: ['./child.component.css']
        })
        export class ChildComponent {
            message = 'Hola Mundo!';
            constructor() { }
        }
        ```

    3. **Child to Parent: Sharing Data via Output() and EventEmitter**
        Another way to share data is to emit data from the child, which can be listened to by the parent. This approach is ideal when you want to share data changes that occur on things like button clicks, form entires, and other user events

        #### parent.component.ts
        ```
        import { Component } from '@angular/core';
        @Component({
            selector: 'app-parent',
            template: `
                Message: {{message}}
                <app-child (messageEvent)="receiveMessage($event)"></app-child>
            `,
            styleUrls: ['./parent.component.css']
        })
        export class ParentComponent {
            constructor() { }
            message:string;
            receiveMessage($event) {
                this.message = $event
            }
        }
        ```

        #### child.component.ts
        ```
        import { Component, Output, EventEmitter } from '@angular/core';
        @Component({
            selector: 'app-child',
            template: `
                <button (click)="sendMessage()">Send Message</button>
            `,
            styleUrls: ['./child.component.css']
        })
        export class ChildComponent {
            message: string = "Hola Mundo!"
            @Output() messageEvent = new EventEmitter<string>();
            constructor() { }
            sendMessage() {
                this.messageEvent.emit(this.message)
            }
        }

        ```

    4. **Unrelated Components: Sharing Data with a Service**
        

    **[⬆ Back to Top](#table-of-contents)**

17. ### Directives
    Directives in Angular is a js class, which is declared as @directive. We have 3 directives in Angular. 
    1. **Component Directives:** These form the main class having details of how the component should be processed, instantiated and used at runtime
    2. **Structural Directives:** A structure directive basically deals with manipulating the dom elements. Structural directives have a * sign before the directive. For example, *ngIf and *ngFor
    3. **Attribute Directives:** Attribute directives deal with changing the look and behavior of the dom element. You can create your own directives as shown below

    ##### Creating Directive:
    ```
    Syntax: ng g directive nameofthedirective

    Eg: ng g directive changeText
    ```

    ##### Usage
    ```
    change-text.directive.ts:

    import { Directive, ElementRef} from '@angular/core';
        @Directive({
            selector: '[changeText]'
        })

        export class ChangeTextDirective {
            constructor(Element: ElementRef) {
                console.log(Element);
                Element.nativeElement.innerText="Text is changed by changeText Directive. ";
            }
        }


    ```

    ```
    app.component.html

    <span changeText >Welcome to {{title}}.</span>
    ```
    **[⬆ Back to Top](#table-of-contents)**

18. ### Lazy loading
    Lazy loading is a technology of angular that allows you to load JavaScript components when a specific route is activated. It improves application load time speed by splitting the application into many bundles. When the user navigates by the app, bundles are loaded as needed
    <br>
    Lazy loading helps to keep the bundle size small, which helps reduce load times <br/>

    **The main properties are:**
    1. **import:** Components of this module are used with Array with other modules
    2. **Declarations:** It receives an array of the components
    3. **Export:** Defines an array of components, directives, and pipes used by other modules
    4. **Provider:** Declares services that are available to the entire application if it is a root module

    **app-routing.module.ts**
    ```
    {  
        path: 'lazy-loading',  
        load children: () => import('./lazy-loading/lazy-loading.module')  
        .then(m => m.LazyLoadingModule)  
    },  
    ```

    **[⬆ Back to Top](#table-of-contents)**

19. ### Observable vs Promises
    Promises and Observables provide us with abstractions that help us deal with the asynchronous nature of our applications<br>
    **Promise**
        A Promise handles a single event when an async operation completes or fails
    **Observable**
        An Observable is like a Stream (in many languages) and allows to pass zero or more events where the callback is called for each event
    **[⬆ Back to Top](#table-of-contents)**

20. ### How to upgrade angular version
    In order to update the angular-cli package installed globally in your system, you need to run
    ```
    npm uninstall -g @angular/cli
    npm install -g @angular/cli@latest

                    OR
    ng update @angular/cli
    ```

    **[⬆ Back to Top](#table-of-contents)**

21. ### How you can apply color to the table rows based on the their status(either true/false) with css
    ```
    HTML::
    <span [ngClass]="status == true ? 'color1' : 'color2'"> change color</span>

    CSS::
    .color1{
        color: red;
    }

    .color2{
        color: green;
    }
    ```
    **[⬆ Back to Top](#table-of-contents)**

22. ### JIT and AOT Compiler in Angular
    An angular application mainly consists of HTML templates, their components which include various TypeScript files. There are some unit testing and configuration file. Whenever we run over an application, the browser cannot understand the code directly hence we have to compile our code

    1. **AOT (Ahead of Time):**
        In simple words, when you serve/build your angular application, the Ahead of Time compiler converts your code during the build time before your browser downloads and runs that code. From Angular 9, by default compiling option is set to true for ahead of time compiler
        **Why should you use the Ahead of Time compiler ?**
        * When you are using Ahead of Time Compiler, compilation only happens once, while you build your project
        * We don’t have to ship the HTML templates and the Angular compiler whenever we enter a new component
        * It can minimize the size of your application
        * The browser does not need to compile the code in run time, it can directly render the application immediately, without waiting to compile the app first so, it provides quicker component rendering
        * The Ahead of time compiler detects template error earlier. It detects and reports template binding errors during the build steps before users can see them
        * AOT provides better security. It compiles HTML components and templates into JavaScript files long before they are served into the client display. So, there are no templates to read and no risky client-side HTML or JavaScript evaluation. This will reduce the chances of injections attacks

    2. **JIT (Just in Time):**
        Just in time compiler provides compilation during the execution of the program at a run time before execution. In simple words, code get compiles when it’s needed, not at the build time
        **Why and When Should you use Just In Time Compiler ?**
        * Just in time compiler compiles each file separately and it’s mostly compiled in the browser. You don’t have to build your project again after changing your code
        * Most compiling is done on the browser side, so it will take less compiling time
        * If you have a big project or a situation where some of your components don’t come in use most of the time then you should use the Just in time compiler
        * Just in Time compiler is best when your application is in local development

    **[⬆ Back to Top](#table-of-contents)**

23. ### Observable
    Angular makes use of observables as an interface to handle a variety of common asynchronous operations

    **[⬆ Back to Top](#table-of-contents)**

24. ### Memory Leak 
    Memory leak is a resource leak that takes place when a computer program/application incorrectly manages memory allocations where memory that are no longer needed are not being properly released

    A memory leak is one of the worst types of issues you can have. It’s hard to find, hard to debug, and often hard to solve
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**

9. ### Bootstrapping
    **[⬆ Back to Top](#table-of-contents)**
    
