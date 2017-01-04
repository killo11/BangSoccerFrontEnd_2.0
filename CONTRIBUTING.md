# Contributing to eMarket 
 
 - [Question or Problem?](#have-a-question-problem-or-idea)
 - [Issues and Bugs](#bug)
 - [Feature Requests](#feature)
 - [Submition Guidelines](#feature)
 - [Guidelines for Developer](#developer)

## <a name="question"></a> Have a Question, Problem, or Idea?
If you have questions or ideas regarding to eMarket, please direct these to the [eMarket Forum](http://forum.emarket.do) "Should be a forum soon"

Otherwise, do you:

- [Found a Bug ?](#bug)
- [Want a Feature ?](#feature)

#### <a name="bug"></a>1. Found a Bug or Issue?
If you find a bug in the source code or a mistake in the documentation, we recommend that you first review the [Online Documentation](http://docs.emarket.do/).

Otherwise you can help us improve by submitting an issue to our
[GitLab Repository](https://gitlab.com/emarket/frontend/issues/new).


## <a name="developer"></a> Developer Guidelines
	
We have a very specific rules over how we create all kind of source file on eMarket. This help us to understand faster our code

 - [Folder Structures](#folders)
 - [Modules](#module)
 - [Injections](#injection)
 - [Controllers](#controller)
 - [States](#state)
 - [Templates](#template)
 - [Services and Factories](#module)
 - [Directives](#module)
 - [Less](#module)
 - [Test](#module)


### <a name="folders"></a> Folder Structure

Our project use the Yeoman generator based on the ngBoilerplate kickstarter, a best-practice boilerplate for any scale Angular project built on a highly modular, folder-by-feature structure. You can find more details on the [Yeoman Generator](https://github.com/thardy/generator-ngbp) and in the [ngBoirlerplate](https://github.com/ngbp/ngbp)

### <a name="module"></a> Modules

We use the folder-by-feature structure thats mean that every folder is a module, all module are created with the emarket prefix example:

 - `angular.module('emarket.module-name')` 

The module name is used in lower case and if we use a compound word must be separate by dash (-)

All module that inherict from `main` module will have the navigation bar, only few module don't use the `main ` module like the `auth` and `register`

### <a name="injection"></a> Injection

The angular injections should be in the following orders

 - First the angular modules
 - Then the third party modules
 - And then your custom modules

### <a name="controller"></a> Controllers

The controllers file name must be in lisp-case and the controller name must be in lower camelCase, not put Ctrl, Controller or any other identifier for refering to Controller.

All controller should stop every listenner on destroy

### <a name="state"></a> State

The state must have in the file `name.module.js` and the name should be in lower case

The url must be in spanish and lisp-case

All the controller on state must be declare as **controller as**

### <a name="templates"></a> Templates

All template must be in lisp-case and end with `.tpl.html`, must be wrap inside a class with the module name or something that identify the view

### <a name="service-factory"></a> Services and Factories

All services and factory must be in CamelCase the name of the file should use the lisp-case and end with .service or .factory accordly example: `my-http-something.services.js`

### <a name="directive"></a> Directives

The directives should start with `em` as a filename with lisp-case and as directive name with `em` with camelCase example `emSuperDirective` as name and as a filename `em-super-directive`


### <a name="less"></a> Less

Every less file should be in lisp-case and must be wrapper inside the main class of his module.

### <a name="Test"></a> Test
>still working on it