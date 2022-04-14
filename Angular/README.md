# Angular Interview Questions & Answers
--------

### Table of Contents

| No. | Questions |
|---- | --------- |
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
|21 | [How you can apply color to the table rows based on the their status(either true/false) with css](#how-you-can-apply-color-to-the-table-rows-based-on-the-their-statuseither-truefalse-with-css)|
|22 | [JIT and AOT](#jit-and-aot)|
|23 | [Observable](#observable)|
|24 | [Memory leak](#memory-leak)|
|25 | [Pipes in angular](#pipes-in-angular)|
|26 | [API calls](#api-calls)|
|27 | [Callback functions](#callback-functions)|
|28 | [Event bubbling](#event-bubbling)|
|29 | [Arrow functions](#arrow-functions)|
|30 | [Pseudo clases](#pseudo-clases)|
|31 | [Positions](#positions)|
|32 | [Angular 10 Main features](#angular-10-Main-features)|
|33 | [Elements](#elements)|
|34 | [Custom Pipes](#custom-pipes)|
|35 | [Route guards](#route-guards)|
|36 | [Difference between service directive and module](#difference-between-service-directive-and-module)|
|37 | [Use of package.json](#use-of-packagejson)|
|38 | [Angular architecture](#angular-architecture)|
|39 | [Wild card routing](#wild-card-routing)|
|40 | [Observables](#observables)|
|41 | [Error handling](#error-handling)|
|42 | [What Is component](#what-is-component)|
|43 | [Interceptors](#interceptors)|
|44 | [Pass headers in request](#pass-headers-in-request)|
|45 | [Is browser understands the typescript directly](#is-browser-understands-the-typescript-directly)|
|46 | [Reactive forms](#reactive-forms)|
|47 | [Template-driven forms](#template-driven-forms)|
|48 | [Auth guard](#auth-guard)|
|49 | [Routing in angular](#routing-in-angular)|
|50 | [Event loop in JavaScript](#event-loop-in-JavaScript)|
|51 | [Let, Var and Const](#let-var-and-const)|
|52 | [Destructuring](#destructuring)|
|53 | [Angular 13 Features](#angular-13-features)|
|54 | [Observables in angular](#observables-in-angular)|
|55 | [Promise in angular](#promise-in-angular)|
|56 | [Subscribe in angular](#subscribe-in-angular)|
|57 | [Subject in angular](#subject-in-angular)|
|57 | [Behaviorsubject in angular](#behaviorsubject-in-angular)|
|57 | [Resolvers in angular](#resolvers-in-angular)|
|** | [HostListener in angular](#hostlistener-in-angular)|
|** | [HostBinding in angular](#hostbinding-in-angular)|
|** | [Position absolute and Position relative](#position-absolute-and-position-relative)|
|** | [Pseudo-Elements and Pseudo-classes](#pseudo-elements-and-pseudo-classes)|
|** | [ES6 Array methods](#es6-array-methods)|
|** | [Form group and Form array](#form-group-and-form-array)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|
|** | [question](#)|



--------
1. ### Hoisting
    Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution

    ```js
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

    ```js
    var a = [1,2,3];

    var b = [ ...a ];		//	Spread syntax (...)
    var c = Array.from(a);
    var d = a.slice();
    ```
    **[⬆ Back to Top](#table-of-contents)**

5. ### Cloning Objects
    2 types to copy object without reference.

    ```js
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
    ```json
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

    ```ts
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
    ```ts
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
    ```ts
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
    
    **Note** switchMap cancels previous HTTP requests that are still in progress, while mergeMap lets all of them finish
    **[⬆ Back to Top](#table-of-contents)**
    
13. ### Map Reduce and Filter

    1. **Map:**
        Map operator takes an observable source as input. It applies a project function to each of the values emitted by the source observable and transforms it into a new value. It then emits the new value to the subscribers

        ```ts
        import { map } from 'rxjs/operators'

        srcArray = from([1, 2, 3, 4]);

        multiplyBy2() {
            this.srcArray
            .pipe(map(val => { return val * 2}))
            .subscribe(val => { console.log(val)})
        }
	
	    // The output is 2,4,6,8
        ```
    2. **Reduce:**
        The reduce() method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array

        ```js
        const numbers = [1, 2, 3, 4];
        const sum = numbers.reduce(function (result, item) {
            return result + item;
        }, 0);

        console.log(sum); // 10
        ```

    3. **Filter:**
        The filter() method takes each element in an array and it applies a conditional statement against it. If this conditional returns true, the element gets pushed to the output array. If the condition returns false, the element does not get pushed to the output array

        ```js
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

    ```ts
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
    ```ts
    async getPrice(currency: string): Promise<any> { 
        return this.httpClient.get<any>("API URL").toPromise(); 
    } 

    this.price = await this.getPrice(this.currency); 
    ```

    2. **Promise:**
    
    #### Syntax:
    ```ts
    var promise = new Promise((resolve, reject) => {
    });
    ```

    #### Ex:
    ```ts
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
        ```ts
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
        ```ts
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
        ```ts
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
        ```ts
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
        ```ts
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
        ```ts
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
    ```ts
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

    ```html
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
    ```ts
    {  
        path: 'lazy-loading',  
        load children: () => import('./lazy-loading/lazy-loading.module')  
        .then(m => m.LazyLoadingModule)  
    },  
    ```

    **[⬆ Back to Top](#table-of-contents)**

19. ### Observable vs Promises
    Promises and Observables provide us with abstractions that help us deal with the asynchronous nature of our applications<br>
    **Promise**<br>
        A Promise handles a single event when an async operation completes or fails<br>
    **Observable**<br>
        An Observable is like a Stream (in many languages) and allows to pass zero or more events where the callback is called for each event
    **[⬆ Back to Top](#table-of-contents)**

20. ### How to upgrade angular version
    In order to update the angular-cli package installed globally in your system, you need to run
    ```ts
    npm uninstall -g @angular/cli
    npm install -g @angular/cli@latest

                    OR
    ng update @angular/cli
    ```

    **[⬆ Back to Top](#table-of-contents)**

21. ### How you can apply color to the table rows based on the their status(either true/false) with css
    ```html
    HTML::
    <span [ngClass]="status == true ? 'color1' : 'color2'"> change color</span>
    ```
    ```css
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

25. ### Pipes in angular
    Decorator that marks a class as pipe and supplies configuration metadata. Angular 4 provides some built-in pipes

    * Lowercasepipe ```{{title | uppercase}} // title```
    * Uppercasepipe ```{{title | lowercase}}    //  TITLE```
    * Datepipe ```{{todaydate | date:'d/M/y'}}  //  14/2/2022```
    * Currencypipe 
    ```js
    {{6589.23 | currency:"USD"}}  
    //  USD6,589.23

    {{6589.23 | currency:"USD":true}}</b> //Boolean true is used to get the sign of the currency.
    $6589.23
      
    ```
    * Jsonpipe ```{{jsonval | json }}   //  {"name": "abc", "age": "50"}```
    * Percentpipe ```{{00.54565 | percent}} //  54.565```
    * Decimalpipe ```{{454.78787814 | number: '3.4-4'}}```
    * Slicepipe 
    ```js
    months = ["Jan", "Feb", "Mar", "April", "May", "Jun",
             "July", "Aug", "Sept", "Oct", "Nov", "Dec"];

    {{months | slice:2:6}}

    Result: Mar, April, May, Jun
    ```

    #### [Custom Pipes](#custom-pipes) See bellow for Custom Pipes

    **[⬆ Back to Top](#table-of-contents)**

26. ### API calls
    Most front-end applications need to communicate with a server over the HTTP protocol, to download or upload data and access other back-end services. Angular provides a client HTTP API for Angular applications, the HttpClient service class in @angular/common/http.

    ```ts
    import { HttpClientModule } from '@angular/common/http';

    constructor(private http: HttpClient) { }

    this.http.get<"Model">("URL");
    ```
    **[⬆ Back to Top](#table-of-contents)**

27. ### Callback functions
    Callback function is a function which is passed to a function as parameter and is executed when the outer function is completed
    ```js
    function useAsCallback(string){
        console.log("callback is being executed with passed parameter: " + string)
    }

    function main(param, callback){
        callback(param)
    }

    main(123456, useAsCallback)

    ```
    **[⬆ Back to Top](#table-of-contents)**

28. ### Event bubbling
    Event bubbling is a method of event propagation in the HTML DOM API when an event is in an element inside another element, and both elements have registered a handle to that event

    **[⬆ Back to Top](#table-of-contents)**

29. ### Arrow functions
    An arrow function expression is a compact alternative to a traditional function expression, but is limited and can't be used in all situations
    ```js
    const materials = [
        'Hydrogen',
        'Helium',
        'Lithium',
        'Beryllium'
    ];
    console.log(materials.map(material => material.length));
    // expected output: Array [8, 6, 7, 9]
    ```

    **[⬆ Back to Top](#table-of-contents)**

30. ### Pseudo Classes
    A pseudo-class is used to define a special state of an element. For example, it can be used to
    * Style an element when a user mouses over it
    * Style visited and unvisited links differently
    * Style an element when it gets focus

    #### Syntax::
    ```
    selector:pseudo-class {
        property: value;
    }
    ```
    #### Eg::
    ```css
    a:link {
        color: #FF0000;
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**

31. ### Position property
    The position property specifies the type of positioning method used for an element
    There are five different position values
    * static
        - HTML elements are positioned static by default. 
        - Static positioned elements are not affected by the top, bottom, left, and right properties
        ```css
        div.static {
            position: static;
        }
        ```
    * relative
        - An element with position: relative; is positioned relative to its normal position
        - Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element
        ```css
        div.static {
            position: relative;
            left: 30px;
        }
    * fixed
        - An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element
        - A fixed element does not leave a gap in the page where it would normally have been located
        ```css
        div.fixed {
            position: fixed;
            bottom: 0;
            right: 0;
        }
        ```
    * absolute
        - An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed)
        - However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling
    * sticky
        - An element with position: sticky; is positioned based on the user's scroll position
        - A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed)

    **[⬆ Back to Top](#table-of-contents)**

32. ### Angular 10 Main features
    1. **Language Service:** 
        The language-service-specific compiler enables multiple typecheck files by using the project interface which creates ScriptInfos as necessary 
    2. **New Default Browser Configuration:** 
        Browser configuration for new projects have been updated to outdo older and less used browsers. This includes the side effect of disabling ES5 builds by default for new projects
    3. **Compiler Update:** 
        In the latest angular version, a compiler interface has been added in order to wrap the actual ngtsc compiler. Angular version 10 has added name spans for property reads and method calls. In addition to this Dependency information, ng-content selectors, Angular Language Service have also been added to the metadata
    4. **Optional Stricter Settings:** 
        Angular version 10 offers a more strict project setup in order to create a new workspace with ng new
        ```
        ng new --strict
        ```
        Once this flag is enabled, it initializes the new project with a couple of new settings that improve maintainability, assist in catching bugs well ahead in time, and permit the CLI to perform advanced optimizations on your app. Enabling this flag configures the app as side-effect free to ensure more advanced tree-shaking
    5. **Ngcc:**
        With this angular 10 feature, there has been an implementation of a Program-based entry-point finder, which is designed to only process entry points that can only be reached by a program defined by a tsconfig.json file
    6. **Performance Improvements:**
        One can see improvement in the performance that is achieved by reducing the size of the entry point. In addition, caching of dependencies is executed within the entry point manifest and are read from there as opposed to being computed each time. Previously, even though an entry point did not need processing, ngcc (Angular Ivy compatibility compiler) might parse the files of the entry point to compute dependencies, which might take a whole lot of time for large_node modules
    7. **Service Workers:**
        In the previous versions of angular Vary headers might have been taken into consideration while retrieving resources from the cache, however absolutely stopping the retrieval of cached assets and main to unpredictable behavior due to inconsistent/buggy implementations in various browsers
    8. **Typescript 3.9, TSLib 2.9 & TSLint v6:**
        Angular 10 features typescript 3.9. As opposed to the previous version which supported typescript 3.6, 3.7 and even 3.8. Typescript is a language that builds on JavaScript by adding syntax for type declarations and annotations which is used by the TypeScript compiler to type-check our code. This in turn clean readable JavaScript that runs on lots of different runtimes
    9. **Localization:**
        One of the best features of Angular 10 is that the latest angular version supports for merging of multiple translation documents which could only load one file in the previous versions
    10. **Router:**
        The CanLoad guard now can go back Urltree in angular version 10. A CanLoad guard returning Urltree cancels the cutting-edge navigation and helps to redirect
    11. **Deprecation:**
        Angular 10 features typescript 3.9. As opposed to the previous version which supported typescript 3.6, 3.7 and even 3.8. Angular 10 also has deprecated the inclusion of ESM5 or FESM5 bundles which saves 119MB of download and install time while running yarn or npm install for Angular packages and libraries. any down leveling to support ES5 in this version will be done at the end of the build process
    **[⬆ Back to Top](#table-of-contents)**

33. ### Elements
    The Angular Elements package (@angular/elements) allows you to create native custom elements and author web components with Angular<br>
    The @angular/elements package provides a createCustomElement() API that can be used to transform Angular Components to native Custom Elements

    **[⬆ Back to Top](#table-of-contents)**

34. ### Custom Pipes
    Angular also has the facility to create custom pipes. The general way to define a custom pipe is as follows

    ```ts
    import { Pipe, PipeTransform } from '@angular/core';  
    @Pipe({name: 'Pipename'}) 

    export class Pipeclass implements PipeTransform { 
        transform(parameters): returntype { } 
    }
    ```

    #### example:
    1. First, create a file called multiplier.pipe.ts
        ```ts
        import { 
            Pipe, 
            PipeTransform 
        } from '@angular/core';  

        @Pipe ({ 
            name: 'Multiplier' 
        }) 

        export class MultiplierPipe implements PipeTransform { 
            transform(value: number, multiply: string): number { 
                let mul = parseFloat(multiply); 
                return mul * value 
            } 
        }
        ```
    2. Usage 
        ```html
        <p>Multiplier: {{2 | Multiplier: 10}}</p>
        ```
    3. Add MultiplierPipe declarations in *app.module.ts* file
        ```ts
        declarations: [AppComponent, MultiplierPipe],
        ```
    **[⬆ Back to Top](#table-of-contents)**

35. ### Route guards
    The Angular router’s navigation guards allow to grant or remove access to certain parts of the navigation. Another route guard, the CanDeactivate guard, even allows you to prevent a user from accidentally leaving a component with unsaved changes
    Here are the 4 types of routing guards available
    1. **CanActivate:** Controls if a route can be activated
    2. **CanActivateChild:** Controls if children of a route can be activated
    3. **CanLoad:** Controls if a route can even be loaded. This becomes useful for feature modules that are lazy-loaded. They won’t even load if the guard returns false
    4. **CanDeactivate:** Controls if the user can leave a route. Note that this guard doesn’t prevent the user from closing the browser tab or navigating to a different address. It only prevents actions from within the application itself

    #### can-activate-route.guard.ts
    ```ts
    import { Injectable } from '@angular/core';
    import {
        CanActivate,
        ActivatedRouteSnapshot,
        RouterStateSnapshot 
    } from '@angular/router';
    import { AuthService } from './auth.service';

    @Injectable()
    export class CanActivateRouteGuard implements CanActivate {
    constructor(private auth: AuthService) {}
    }
    ```

    #### app-routing.module.ts
    ```ts
    import { CanActivateRouteGuard } from './can-activate-route.guard';
    const routes: Routes = [
        { path: '', component: HomeComponent },
        { path: 'dashboard',
            component: DashboardComponent,
            canActivate: [CanActivateRouteGuard]
        }
    ]
    ```

    **[⬆ Back to Top](#table-of-contents)**

36. ### Difference between service directive and module
    1. Modules
        * provide a way to namespace/group services, directives, filters, configuration information and initialization code
    2. Services
        * are singletons, so there is only one instance of each service you define. As singletons, they are not affected by scopes, and hence can be accessed by (shared with) multiple views/controllers/directives/other services
        * To use a service, dependency injection is required on the dependent (e.g., on the controller, or another service, or a directive).
    3. Directives 
        * are responsible for updating the DOM when the state of the model changes
        * Directives allow you to "componentize HTML". Directives are often better than ng-include. E.g., when you start writing lots of HTML with mainly data-binding, refactor that HTML into (reusable) directives
    **[⬆ Back to Top](#table-of-contents)**

37. ### Use of package.json
    Once you create new Angular application, you will see package.json file among the newly created files and folders. package.json file locates in project root and contains information about your web application. The main purpose of the file comes from its name package, so it'll contain the information about npm packages installed for the project.
    Let's take a look at main sections in package.json file.
    1. **Project Metadata:** 
        Metadata contains information about your application
        ```json
        "name": "my-first-angular-app",
        "version": "0.0.0",
        "private": true,
        ```
    2. **Scripts:**
        This section describes Node scripts you can run in your application. As the code sample uses Angular CLI, all scripts are calling it.
        ```json
        "scripts": {
            "ng": "ng",
            "start": "ng serve",
            "build": "ng build",
            "test": "ng test",
            "lint": "ng lint",
            "e2e": "ng e2e"
        },
        ```
    3. **Dependencies:** 
        The list of packages installed as dependencies for this project are required at runtime
        ```json
        "dependencies": {
            "@angular/animations": "~8.0.1",
            "@angular/common": "~8.0.1",
            "@angular/compiler": "~8.0.1",
            "@angular/core": "~8.0.1",
            "@angular/forms": "~8.0.1",
            "@angular/platform-browser": "~8.0.1",
            "@angular/platform-browser-dynamic": "~8.0.1",
            "@angular/router": "~8.0.1",
            "rxjs": "~6.4.0",
            "tslib": "^1.9.0",
            "zone.js": "~0.9.1"
        },
        ```
    4. **Development Dependencies:**
        The list of packages that are required only for development. This packages are installed only on developer's machine and will not be run for production build
        ```json
        "devDependencies": {
            "@angular-devkit/build-angular": "~0.800.0",
            "@angular/cli": "~8.0.3",
            "@angular/compiler-cli": "~8.0.1",
            "@angular/language-service": "~8.0.1",
            "@types/node": "~8.9.4",
            "@types/jasmine": "~3.3.8",
            "@types/jasminewd2": "~2.0.3",
            "codelyzer": "^5.0.0",
            "jasmine-core": "~3.4.0",
            "jasmine-spec-reporter": "~4.2.1",
            "karma": "~4.1.0",
            "karma-chrome-launcher": "~2.2.0",
            "karma-coverage-istanbul-reporter": "~2.0.1",
            "karma-jasmine": "~2.0.1",
            "karma-jasmine-html-reporter": "^1.4.0",
            "protractor": "~5.4.0",
            "ts-node": "~7.0.0",
            "tslint": "~5.15.0",
            "typescript": "~3.4.3"
        }
        ```

    **[⬆ Back to Top](#table-of-contents)**

38. ### Angular architecture
    Angular is a platform and framework for building single-page client applications using HTML and TypeScript. Angular is written in TypeScript. It implements core and optional functionality as a set of TypeScript libraries that you import into your applications
    The Eight main building blocks of an Angular application
    1. **Modules:** Every Angular app has a root module, conventionally named AppModule, which provides the bootstrap mechanism that launches the application. An app typically contains many functional modules
    2. **Components:** Every Angular project has at least one component, the root component and root component connects the component hierarchy with a page document object model (DOM). Each component defines the class that contains application data and logic, and it is associated with the HTML template that defines the view to be displayed in a target app.A component controls a patch of screen called a view
        ```ts
        // app.component.ts
        @Component({
            selector: 'app-root',
            templateUrl: './app.component.html',
            styleUrls: ['./app.component.css']
        })
        ```
    3. **Templates:** The angular template combines the HTML with Angular markup that can modify HTML elements before they are displayed. Template directives provide program logic, and binding markup connects your application data and the DOM. There are two types of data binding
        * **Event binding** lets your app respond to user input in the target environment by updating your application data
        * **Property binding** lets you interpolate values that are computed from your application data into the HTML
        ```html
        <div style="text-align:center">
        <h1>
            {{2 | power: 5}}
        </h1>
        </div>
        ```
    4. **Metadata:** Metadata tells Angular how to process a class.It is used to decorate the class so that it can configure the expected behavior of a class. Decorators are the core concept when developing with Angular (versions 2 and above)
        ```ts
        // app.component.ts
        @Component({
            selector: 'app-root',
            templateUrl: './app.component.html',
            styleUrls: ['./app.component.css']
        })
        ```
    5. **Data binding:** Data binding plays an important role in communication between a template and its component
        * **From the Component to the DOM** 
            Interpolation: {{ value }}: Interpolation adds the value of the property from the component
            ```html
            <p>Name: {{ student.name }}</p>
            ```
        * **Property binding: [property]=”value”**
            With property binding, a value is passed from a component to a specified property, which can often be a simple html attribute
            ```html
            <input type="text" [value]="student.name" />
            ```
        * **Event binding: (Event)=”myFunction($event)”**
            With Event binding, a value is passed from a child Component to Parent Component,which can often be a simple html attribute
            ```html
            <input type="text" (myEvent)="onClick($event)" />
            ```
        * **Two-Way binding: [(ngModel)]=”property”**
            It is an important fourth form that combines property and event binding in a single notation, using the ngModel directive
            ```html
            <input [(ngModel)]="hero.name">
            ```
    6. **Directives:** An Angular component isn’t more than a directive with the template. When we say that components are the building blocks of Angular applications, we are saying that directives are the building blocks of Angular projects. Let us use built-in Angular directive like ngClass, which is a better example of the existing Angular attribute directive
        [⬆ ReadHere](#directives)**
    7. **Services:** For data or logic that isn’t associated with a specific view, and that you want to share across components, you create a service class. The @Injectable decorator immediately precedes the service class definition
    8. **Dependency injection:** Dependencies are services or objects that a class needs to perform its function. Dependency injection, or DI, is a design pattern in which a class requests dependencies from external sources rather than creating them
    **[⬆ Back to Top](#table-of-contents)**

39. ### Wild card routing
    The Wildcard Route is basically used in Angular Application to handle the invalid URLs. Whenever the user enter some invalid URL or if you have deleted some existing URL from your application, then by default 404 page not found error page is displayed. In such scenarios instead of showing the default error page, if you also show a custom error page and this is possible by using the Angular Wildcard Route
    ```ts
    const routes: Routes = [
        {
            path:'**', component:CustomerrorComponent
        },
        {
            path:'', redirectTo:'Login',pathMatch:'full'
        },
    ]
    ```
    **[⬆ Back to Top](#table-of-contents)**

40. ### Observables
    Angular makes use of observables as an interface to handle a variety of common asynchronous operations. For example
    * You can define custom events that send observable output data from a child to a parent component
    * The HTTP module uses observables to handle AJAX requests and responses
    * The Router and Forms modules use observables to listen for and respond to user-input events
    **[⬆ Back to Top](#table-of-contents)**

41. ### Error handling
    Handling errors properly is essential in building a robust application in Angular. Error handlers provide an opportunity to present friendly information to the user and collect important data for development
    An application that does not handle errors gracefully leaves its users confused and frustrated when the app suddenly breaks without explanation. Handling these errors correctly across an application greatly improves user experience
    There are two types of error handling mechanism in Angular. One catches all the client side errors and the other one catches the HTTP Errors
        * **HTTP Errors**
            The HTTP Errors are thrown, when you send a HTTP Request using the HttpClient Module. The errors again falls into two categories. One is generated by the server like unauthorized user, session expired, Server down etc. The Other one is generated at the client side, while trying to generate the HTTP Request. These errors could be network error, error while generating the request etc
        * **Client Side Errors**
            All other errors thrown by the code falls into this category. These are handled by the **ErrorHandler** class, which is the default error handler for Angular
    **[⬆ Back to Top](#table-of-contents)**

42. ### What Is component
    Components are the main building block for Angular applications. Each component consists of
    * An HTML template that declares what renders on the page
    * A Typescript class that defines behavior
    * A CSS selector that defines how the component is used in a template
    * Optionally, CSS styles applied to the template

    #### Creating a component using the Angular CLI
    Run the ```ng generate component <component-name>``` command, where ```<component-name>``` is the name of your new component
    By default, this command creates the following
    * A folder named after the component
    * A component file, ```<component-name>.component.ts```
    * A template file, ```<component-name>.component.html```
    * A CSS file, ```<component-name>.component.css```
    * A testing specification file, ```<component-name>.component.spec.ts```

    #### Creating a component manually
    Although the Angular CLI is the best way to create an Angular component, you can also create a component manually

    **[⬆ Back to Top](#table-of-contents)**

43. ### Interceptors
    The Angular HTTP interceptors sit between our application and the backend. When the application makes a request, the interceptor catches the request before it is sent to the backend. By Intercepting requests, we will get access to request headers and the body. This enables us to transform the request before sending it to the Server
    **[⬆ Back to Top](#table-of-contents)**

44. ### Pass headers in request
    HTTP Headers let the client and the server share additional information about the HTTP request or response. For example, we use the content-type header to indicate the media type of the resource like JSON, text, blob, etc. Another important header is where you send the bearer token using the Authorization header
    We add HTTP Headers using the HttpHeaders helper class. It is passed as one of the arguments to the GET, POST, PUT, DELETE, PATCH & OPTIONS request

    ```ts
    import { HttpHeaders } from '@angular/common/http';

    const headers= new HttpHeaders()
        .set('content-type', 'application/json')
        .set('Access-Control-Allow-Origin', '*');

    //calling
    this.httpClient.get("URL", { 'headers': headers })
    ```
    **[⬆ Back to Top](#table-of-contents)**

45. ### Is browser understands the typescript directly
    Typescript cannot be run or understood in any browser. So, Typescript is compiled to Javascript (which browsers can understand). Typescript can use all ES6 features and during the compilation they will be converted to Target compile options like ES5
    **[⬆ Back to Top](#table-of-contents)**

46. ### Reactive forms
    * **Reactive forms:** Reactive forms are forms where we define the structure of the form in the component class. I,e we create the form model with Form Groups, Form Controls, and Form Arrays. We also define the validation rules in the component class. Then, we bind it to the HTML form in the template
    #### How to use Reactive Forms
    1. **Import ReactiveFormsModule**
        To work with Reactive forms, we must import the ReactiveFormsModule. We usually import it in root module or in a shared module
        ```ts
        //AppModel
        import { ReactiveFormsModule } from '@angular/forms';

        @NgModule({
            declarations: [
                AppComponent
            ],
            imports: [
                BrowserModule,
                AppRoutingModule,
                ReactiveFormsModule
            ],
            providers: [],
            bootstrap: [AppComponent]
        })
        ```
    2. **Create Form Model in component class using Form Group, Form Control & Form Arrays**
        In the template-driven approach, we used ngModel & ngModelGroup directive on the HTML elements. The FormsModule created the FormGroup & FormControl instances from the template. This happens behind the scene
        In Reactive Forms approach, It is our responsibility to build the Model using FormGroup, FormControl and FormArray
        ```ts
        import { FormGroup, FormControl, Validators } from '@angular/forms'

        contactForm = new FormGroup({
            firstname: new FormControl(),
            lastname: new FormControl(),
            email: new FormControl(),
        })

        contactFormWithValidation = new FormGroup({
            firstname: new FormControl('', [Validators.required,Validators.minLength(10)]),
            lastname: new FormControl(),
            email: new FormControl(),
        })
        ```
    3. **Create the HTML Form resembling the Form Model**
        ```html
        <form>
            <p>
                <label for="firstname">First Name </label>
                <input type="text" id="firstname" name="firstname">
            </p>
            <p>
                <label for="lastname">Last Name </label>
                <input type="text" id="lastname" name="lastname">
            </p>
            <p>
                <label for="email">Email Id </label>
                <input type="text" id="email" name="email">
            </p>
            <p>
                <button type="submit">Submit</button>
            </p>
        </form>
        ```
    4. **Bind the HTML Form to the Form Model**
        ```html
        <form [formGroup]="contactForm" (ngSubmit)="onSubmit()">
            <p>
                <label for="firstname">First Name </label>
                <input type="text" id="firstname" name="firstname" formControlName="firstname">
            </p>
            <p>
                <label for="lastname">Last Name </label>
                <input type="text" id="lastname" name="lastname" formControlName="lastname">
            </p>
            <p>
                <label for="email">Email Id </label>
                <input type="text" id="email" name="email" formControlName="email">
            </p>
            <p>
                <button type="submit">Submit</button>
            </p>
        </form>
        ```

        ```ts
        onSubmit() {
            console.log(this.contactForm.value);
        }
        ```

    **[⬆ Back to Top](#table-of-contents)**

47. ###  Template-driven forms
    In Template Driven Forms we specify behaviors/validations using directives and attributes in our template and let it work behind the scenes. All things happen in Templates hence very little code is required in the component class. This is different from the reactive forms, where we define the logic and controls in the component class

    1. **Import FormsModule**
    To work with Template-driven forms, we must import the FormsModule. We usually import it in root module or in a shared module.
    ```ts
    //app.module.ts

    import { FormsModule } from '@angular/forms';        //import FormsModule

    @NgModule({
        declarations: [
            AppComponent
        ],
        imports: [
            BrowserModule,
            AppRoutingModule,
            FormsModule              
        ],
        providers: [],
        bootstrap: [AppComponent]
    })
    ```
    2. **HTML Form**
        ```html
        <form>
            <p>
                <label for="firstname">First Name </label>
                <input type="text" id="firstname" name="firstname">
            </p>
            <p>
                <label for="lastname">Last Name </label>
                <input type="text" id="lastname" name="lastname">
            </p>
            <p>
                <label for="email">Email Id </label>
                <input type="text" id="email" name="email">
            </p>
            <p>
                <button type="submit">Submit</button>
            </p>
        </form>
        ```

    **[⬆ Back to Top](#table-of-contents)**

48. ### Auth guard
    AuthGuard is used to protect the routes from unauthorized access in angular.
    Auth guard provide lifecycle event called canActivate. The canActivate is like a constructor. It will be called before accessing the routes. The canActivate has to return true to access the page. If it returns false, we can not access the page
    ```ts
    { path: "create", component: PostCreateComponent, canActivate: [AuthGuard]}
    ```
    
    **[⬆ Back to Top](#table-of-contents)**

49. ### Routing in angular
    Angular provides extensive set of navigation feature to accommodate simple scenario to complex scenario. The process of defining navigation element and the corresponding view is called Routing. Angular provides a separate module, RouterModule to set up the navigation in the Angular application
    * **Creating routes**
        ```ts
        const routes: Routes = [
            { path: 'about', component: AboutComponent },
        ];
        ```
    * **Accessing routes**
        * Include router-outlet tag in the root component template
        ```html
        <router-outlet></router-outlet>
        ```
        * Use routerLink and routerLinkActive property in the required place
        ```html
        <a routerLink="/about" routerLinkActive="active">First Component</a>
        ```
    
    **[⬆ Back to Top](#table-of-contents)**
    
50. ### Event loop in JavaScript
    The event loop is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading. Let’s take a look at what happens on the back-end.
    The call stack is responsible for keeping track of all the operations in line to be executed. Whenever a function is finished, it is popped from the stack
    The event queue is responsible for sending new functions to the stack for processing. It follows the queue data structure to maintain the correct sequence in which all operations should be sent for execution
    **[⬆ Back to Top](#table-of-contents)**

51. ### Let, Var and Const
    * **var** The var is the oldest keyword to declare a variable in JavaScript
    The scope of the var keyword is the global or function scope. It means variables defined outside the function can be accessed globally, and variables defined inside a particular function can be accessed within the function
    * **let** The let keyword is an improved version of the var keyword
    The scope of a let variable is only block scoped. It can’t be accessible outside the particular block
    * **const** The const keyword has all the properties that are the same as the let keyword, except the user cannot update it
    When users declare a const variable, they need to initialize it, otherwise, it returns an error. The user cannot update the const variable once it is declared

    | var | let | const |
    | ------ | ------ | ------|
    | Variables declared with var are in the function scope | Variables declared as let are in the block scope | Variables declared as const are in the block scope |
    | Reassign the value Allowed | Reassign the value Allowed | Reassign the value is Not Allowed for variables, but can allow for objects  |
    | Hosting is Allowed | Hosting is Not Allowed | Hosting is Not Allowed |
    | Redeclaration of the variable Allowed | Redeclaration of the variable Not Allowed | Redeclaration of the variable Not Allowed |
    **[⬆ Back to Top](#table-of-contents)**

52. ### Destructuring
    Destructuring is a way of extracting values into variables from data stored in objects and arrays
    ```ts
    const obj = {text1: 'abc', text2: 'bbb', age: 39 };

    const t1 = obj.text1;
    console.log(t1);         //Output: abc

    const t2 = obj.text2;
    console.log(t2);         //Output: bbb

    const {text1: t11, text2: t12} = obj;
    console.log(t11);         //Output: abc
    console.log(t12);         //Output: bbb
    ```
    **[⬆ Back to Top](#table-of-contents)**

1. ### Angular 13 Features
    * Angular 13 Latest Features
    * TypeScript 4.4 Support in angular13.
    * Form Validation Improvements.
    * Changes to APF.
    * Enhancements to Angular Tests.
    * 100% Ivy and No More Support for View Engine.
    * End of IE11 Support.
    * Update Component API's.
    * Router Improvements.
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Observables in angular
    Observable in Angular is a feature that provides support for delivering messages between different parts of your single-page application. This feature is frequently used in Angular because it is responsible for handling multiple values, asynchronous programming in Javascript, and also event handling processes
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Promise in angular
    A promise is a placeholder for a future value. It serves the same function as callbacks but has a nicer syntax and makes it easier to handle errors.<br>
    Promises can be executed by calling the then() and catch() methods. The then() method takes two callback functions as parameters and is invoked when a promise is either resolved or rejected. The catch() method takes one callback function and is invoked when an error occurs

    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Subscribe in angular
    Subscribe() is a method in Angular that connects the observer to observable events. Whenever any change is made in these observable, a code is executed and observes the results or changes using the subscribe method. Subscribe() is a method from the rxjs library, used internally by Angular
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Subject in angular
    A Subject is a special type of Observable that allows values to be multicasted to many Observers. The subjects are also observers because they can subscribe to another observable and get value from it, which it will multicast to all of its subscribers. Basically, a subject can act as both observable & an observer.

    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Behaviorsubject in angular
    BehaviorSubject is both observer and type of observable. BehaviorSubject always need an initial/default value. Every observer on subscribe gets current value. Current value is either latest value emitted by source observable using next() method or initial/default value<br>
    BehaviorSubject is a type of subject, a subject is a special type of observable so you can subscribe to messages like any other observable. The unique features of BehaviorSubject are:
    * It needs an initial value as it must always return a value on subscription even if it hasn't received a next()
    * Upon subscription, it returns the last value of the subject. A regular observable only triggers when it receives an onnext
    * at any point, you can retrieve the last value of the subject in a non-observable code using the getValue() method
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Resolvers in angular
    Angular Resolver is used for pre-fetching some of the data when the user is navigating from one route to another. It can be defined as a smooth approach for enhancing user experience by loading data before the user navigates to a particular component
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### HostListener in angular
    In Angular, the @HostListener() function decorator allows you to handle events of the host element in the directive class<br>
    Let's take the following requirement: when you hover you mouse over the host element, only the color of the host element should change. In addition, when the mouse is gone, the color of the host element should change to its default color. To do this, you need to handle events raised on the host element in the directive class. In Angular, you do this using @HostListener() 
    ```ts
    @HostListener('mouseover') onMouseOver() {
        this.ChangeBgColor('red');
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**
    
1. ### HostBinding in angular
    In Angular, the @HostBinding() function decorator allows you to set the properties of the host element from the directive class<br>
    Let's say you want to change the style properties such as height, width, color, margin, border, etc., or any other internal properties of the host element in the directive class. Here, you'd need to use the @HostBinding() decorator function to access these properties on the host element and assign a value to it in directive class.
    ```ts
    @HostBinding('style.border') border: string;

    @HostListener('mouseover') onMouseOver() {
        this.border = '5px solid green';
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**
    
1. ### position absolute and position relative
    **position: relative** places an element relative to its current position without changing the layout around it, whereas **position: absolute** places an element relative to its parent's position and changing the layout around it
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Pseudo-Elements and Pseudo-classes
    **Pseudo-Elements**: pseudo-element is used to style specified parts of an element. For example, it can be used to
    * Style the first letter, or line, of an element
    ```css
    p::first-line {
        color: #ff0000;
        font-variant: small-caps;
    }
    p::first-letter {
        color: #ff0000;
        font-size: xx-large;
    }
    ```
    * Insert content before, or after, the content of an element 
    
    | Selector | Example | Description |
    | -------- | ------- | ----------- |
    | ::after | p::after | Insert something after the content of each **< p >** element |
    | ::before | p::before | Insert something before the content of each **< p >** element |
    | ::first-letter | p::first-letter | Selects the first letter of each **< p >** element |
    | ::first-line | p::first-line | Selects the first line of each **< p >** element |
    | ::marker | ::marker | Selects the markers of list items |
    | ::selection | p::selection | Selects the portion of an element that is selected by a user |


    **Pseudo-classes**: pseudo-class is used to define a special state of an element. For example, it can be used to:
    * Style an element when a user mouses over it
    * Style visited and unvisited links differently
    * Style an element when it gets focus
    ```css
    a:link {
        color: #FF0000;
    }
    a:visited {
        color: #00FF00;
    }
    a:hover {
        color: #FF00FF;
    }
    a:active {
        color: #0000FF;
    }
    ```

    **[⬆ Back to Top](#table-of-contents)**
    
1. ### ES6 Array methods
    Some new array methods are introduced in ES6, such as
    * **Array.from():** It converts array-like values and iterable values into arrays
        The general function of this method is to enable new array creation from an array-like object. It converts array-like values and iterable values (such as set and map) into arrays.
        ```js
        let name = Array.from('javaTpoint')  

        console.log(name)   // ['j', 'a', 'v', 'a', 'T', 'p', 'o', 'i', 'n', 't']
        ```
    * **Array.of():** It creates an instance from a variable number of arguments instead of the number of arguments or type of arguments
        In ES5, when a single numeric value gets passed in the array constructor, then it will create an array of that size. Array.of() is a new way of creating an array which fixes this behavior of ES5.

        By using this method, if you are creating an array only with a single numeric value, then it will create an array only with that value instead of creating the array of that size
        ```js
        let name = Array.of(42)

        console.log(name)   // [42]
        console.log(name.length)    // 1
        ```
    * **Array.prototype.copyWithin():** It copies the part of an array to a different location within the same array 
        It is an interesting method that is added to the library of array methods in ES6. This method copies the part of an array to a different location within the same array
        #### Syntax:
        ```js
        array.copyWithin(target, start, end)
        ```
        #### Eg:
        ```js
        const num = [1,2,3,4,5,6,7,8,9,10];  

        console.log(num.copyWithin(1,3,5)); // [1, 4, 5, 4, 5, 6, 7, 8, 9, 10]
        console.log(num.copyWithin(1,3)); // [1, 4, 5, 6, 7, 8, 9, 10, 9, 10]
        ```
    * **Array.prototype.find():** It finds a value from an array, based on the specific criteria that are passed to this method.
        It is another new function of ES6. It finds a value from an array, based on the specific criteria that are passed to this method. It returns the first element value that satisfies the given condition
        #### Syntax:
        ```js
        array.find(callback(currentValue, index, arr),thisValue) 
        ```
        #### Eg:
        ```js
        var arr=[5,22,19,25,34];
        var result=arr.find(x=>x>20);
        console.log(result);    // 22
        ```
    * **Array.prototype.findIndex():** The Array.prototype.findIndex() returns the index of the first element of the given array that satisfies the given condition<br>
        The Array.prototype.findIndex() method returns the index of the first element of the given array that satisfies the given condition. If no element satisfies the condition, then it returns -1.
        #### Syntax:
        ```js
        array.findIndex(callback(value,index,arr),thisArg)
        ```
        #### Eg:
        ```js
        var arr=[5,22,19,25,34];
        var result=arr.findIndex(x=>x>20);
        console.log(result)
        ```
    * **Array.prototype.entries():** It returns an array iterator object, which can be used to loop through keys and values of arrays
        This method returns an array iterator object, which can be used to loop through keys and values of arrays
        Entries will return an array of arrays, in which every child array is an array of [index, value].
        #### Syntax:
        ```js
        array.entries() 
        ```
        #### Eg:
        ```js
        var colours = ["Red", "Yellow", "Blue", "Black"];
        var show = colours.entries();

        // case 1
        for (i of show) {  
            console.log(i);  
        }  

        OR
        // case 2
        console.log(...show);

        OUTPUT::
        [0, 'Red']
        [1, 'Yellow']
        [2, 'Blue']
        [3, 'Black']
        ```
    * **Array.prototype.keys():** It returns an array iterator object along with the keys of the array
        This method works similarly to the Array.entries() method. As its name implies, it is used to return an array iterator object along with the keys of the array
        #### Syntax:
        ```js
        array.keys() 
        ```
        #### Eg:
        ```js
        var colours = ["Red", "Yellow", "Blue", "Black"];
        var show = colours.keys();
        console.log(...show);   // 0 1 2 3
        ```
    * **Array.prototype.values():** it provides the value of each key
        This method is similar to Array.keys() and Array.entries() except that it provides the value of each key
        #### Syntax:
        ```js
        array.values() 
        ```
        #### Eg:
        ```js
        var colours = ["Red", "Yellow", "Blue", "Black"];
        var show = colours.values();
        console.log(...show);   // Red Yellow Blue Black
        ```
    * **Array.prototype.fill():** It fills the specified array elements with a static value
        This method fills the specified array elements with a static value. The value can be used to fill a part of an array or to fill the entire array. It modifies the original array
        #### Syntax:
        ```js
        array.fill(value, start, end)  
        ```
        #### Eg:
        ```js
        var colours = ["Red", "Yellow", "Blue", "Black"];
        var show = colours.fill("Green",2,4);  
        console.log(...show);   // Red Yellow Green Green
        ```
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Form group and Form array
    **FormGroup**
    FormGroup is one of the three fundamental building blocks used to define forms in Angular, along with FormControl and FormArray . When instantiating a FormGroup , pass in a collection of child controls as the first argument. The key for each child registers the name for the control<br>
    **FormArray**
    The FormArray is a way to Manage collection of Form controls in Angular. The controls can be FormGroup, FormControl, or another FormArray. Because it is implemented as Array, it makes it easier dynamically add controls
    **[⬆ Back to Top](#table-of-contents)**


1. ### Pure and Impure Pipes
    **[⬆ Back to Top](#table-of-contents)**

1. ### Doctype and Meta data
    **[⬆ Back to Top](#table-of-contents)**

1. ### Local storage, Session storage and Cookies
    **[⬆ Back to Top](#table-of-contents)**

1. ### Difference between one way data binding and two way data binding
    **[⬆ Back to Top](#table-of-contents)**

1. ### Difference between angular and react js
    **[⬆ Back to Top](#table-of-contents)**
1. ### Question
    **[⬆ Back to Top](#table-of-contents)**

1. ### Question
    **[⬆ Back to Top](#table-of-contents)**
    
1. ### Question
    **[⬆ Back to Top](#table-of-contents)**
