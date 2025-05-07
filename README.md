# Angular Interview - Notes

# 1. What is Angular Module:
An Angular module is a container that groups related components, directives, pipes, and services. It helps organize the application into cohesive blocks and manages dependencies. Every Angular app has at least one root module (AppModule), and you can create feature modules to keep code modular and maintainable.
After angular 14 we can have an app without a module instead you can have standalone component and bootstrap the component . A standalone component is not tied to any module and you can use this component anywhere in the applicaiton by just importing it. The below are the metadata required to create a module
1. declarations - list of components, pipes, directives comes under this module
2. import - list of depencies needed to run this module which will be imported from another modules either modules of the application or external modules like RoutModuel, FormsModule, BrowserModule etc
3. export - list of the components, directives and pipes which can be exported from the module
4. bootstrap - will have the details of the component which can be used to launch this module, this component will be the starting point for this module
5. providers - the array will have the list of services will be required to inject when needed.

#2. What are angular components:
An angular component is one of the building block or key element in angular app. A component refers to controlling one part/section of the application. These are used for human interatctions and displaying the content. In Angular you can create a component by using the @Component decorator in a class file. The component will have the below main parts
1. templateUrl or template
2. styleUrls
3. selector.

Before Angular 14 a component should be part of a module but after angular 14 you can create standalone components which need not be part of any module and use anywhere in the applicatoin by just exporting and importing. 



