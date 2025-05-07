# Angular Interview - Notes

# 1. What is Angular Module:
An Angular module is a container that groups related components, directives, pipes, and services. It helps organize the application into cohesive blocks and manages dependencies. Every Angular app has at least one root module (AppModule), and you can create feature modules to keep code modular and maintainable.
After angular 14 we can have an app without a module instead you can have standalone component and bootstrap the component . A standalone component is not tied to any module and you can use this component anywhere in the applicaiton by just importing it. The below are the metadata required to create a module
1. declarations - list of components, pipes, directives comes under this module
2. import - list of depencies needed to run this module which will be imported from another modules either modules of the application or external modules like RoutModuel, FormsModule, BrowserModule etc
3. export - list of the components, directives and pipes which can be exported from the module
4. bootstrap - will have the details of the component which can be used to launch this module, this component will be the starting point for this module
5. providers - the array will have the list of services will be required to inject when needed.

# 2. What are angular components:
An Angular component is a key building block in an Angular application. It controls one specific part or section of the UI. Components handle user interactions, display data, and contain logic to control that part of the application.
A component is defined using the @Component decorator and consists of:
1. selector: the HTML tag used to insert this component
2. template or templateUrl: defines the HTML structure
3. styleUrls: contains CSS or styling info
4. A TypeScript class for component logic

Before Angular 14, every component had to be part of an Angular module. From Angular 14 onward, standalone components can be created without needing to be declared in a module, making them more reusable and lightweight.

# 3. What are angular services
These are plain typescript files created with @Injectable decorator, has common/reusable code , data access methods, any validations. These can be injected at root level or component level.
@Injectable({
provideIn: 'root'
})
when we provideIn root then you can directly use in any component. If you want to use for module or componnet specific then declare in providers array.
If a service is provided both in 'root' and in a component's providers, Angular uses the component-scoped instance within that component and its subtree, effectively overriding the global singleton.


