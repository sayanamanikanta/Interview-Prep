# Infosys Angular Interview Questions & Answers
--------

### Table of Contents

| No. | Questions |
|---- | ---------|
|1  | [Questions?](#Questions)|
--------

1. ### What is router
    Routing in Angular helps us navigate from one view to another as users perform tasks in web apps.

    To handle the navigation from one view to the next, you use the Angular Router. The Router enables navigation by interpreting a browser URL as an instruction to change the view

    * **Creating routes**
    ```ts
    const routes: Routes = [
        { path: 'about', component: AboutComponent },
    ];
    ```
    * **Accessing routes**
        * Include router-outlet tag in the root component template
        ```ts
        <router-outlet></router-outlet>
        ```
        * Use routerLink and routerLinkActive property in the required place
        ```ts
        <a routerLink="/about" routerLinkActive="active">First Component</a>
        ```
    **[⬆ Back to Top](#table-of-contents)**


1. ### What is ngModule
    An Angular module is a deployment sub-set of your whole Angular application. Its useful for splitting up an application into smaller parts and lazy load each separately, and to create libraries of components that can be easily imported into other applications

    **The NgModule decorator has five important(among all) options**
    * The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application
    * The declarations option is used to define components in the respective module
    * The bootstrap option tells Angular which Component to bootstrap in the application
    * The providers option is used to configure set of injectable objects that are available in the injector of this module
    * The entryComponents option is a set of components dynamically loaded into the view

1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions
1. ### Questions