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
    **Promise**
        A Promise handles a single event when an async operation completes or fails
    **Observable**
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
    
