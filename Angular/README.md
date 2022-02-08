# Angular Interview Questions & Answers
--------

### Table of Contents

| No. | Questions |
|---- | ---------
|1 | [Hoisting?](#hoisting)|
|2 | [Closure?](#closure)|
|3 | [Ngrx?](#ngrx)|


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
    
13. ### map, reduce and filter
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
