# angularInterview

1. What is Angular Module:
   
Angular module is a building block of an angular app. A module will have collection of components, directives, services, pipes etc . Usually a module refers to a independent   functionality inside the app. For example, if we are buidling app for restruant then we can divide the below as modules
    Menu, Cart, Today specials etc. 
Advantages of module - Modualrity of the code, easy to maintain, as angular supports lazy loading of modules it will help the app to load faster. If we have common code to be shared accross the application , we can have module for common components, services, directives etc. Then this module can be used as dependency in other modules.
To make a class as a module we can use @NgModule decorator and this decorator takes the below object.

@Ngmodule({
  'declarations', - this is in array takes list of all the components created under this module
  'providers' - this is in array which will take the list of the services,pipes needed for this module
  'imports' - this is in array which will take the list of depencies needed for this module from other module
  'exports' - this is in array which will have the list of components, services, pipes etc which will be exported so that other modules can use it
  'bootstrap' - this is in array which will take the one component which needs to be intiiliaed when the module loads
})
