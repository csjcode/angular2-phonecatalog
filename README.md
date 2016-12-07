# angular2-phonecatalog
Angular2 phone catalog


### Instructions

* (finished example) git clone --depth=16 https://github.com/angular/angular-phonecat.git
* npm install
* npm start
* http://localhost:8000/index.html

### Step 0

* (back to step 0) git checkout -f step-0
* npm install
* npm start
* http://localhost:8000/index.html
* in app/index.html
* <html ng-app> ng-app attribute represents an Angular directive
* (call angular script) <script src="bower_components/angular/angular.js"></script>
* (binding simple expression) {{'yet' + '!'}} - code snippets that are evaluated by Angular in the context of the current model scope

3 important things that happen during the bootstrap phase:
* The injector that will be used for dependency injection is created.
* The injector will then create the root scope that will become the context
* Angular will then "compile" the DOM starting at the ngApp root element processing any directives and bindings found along the way.

* Add: <p>1 + 2 = {{1 + 2}}</p>

### Step 1

* Add new html per tutorial
* Add new CSS file link in html file
* In Angular, the view is a projection of the model through the HTML template.

### Step 2 - Angular Template basic structure

* Update index.html - <html ng-app="phonecatApp">
* Update index.html - <body ng-controller="PhoneListController">
* Update index.html - <li ng-repeat="phone in phones"><span>{{phone.name}}</span><p>{{phone.snippet}}</p></li>
* Creat Model: app.js file, add code
* Test it: app/app.spec.js: add new code
* npm test
* testing is off because I started with some other tests in there (from later in the tut).

### Step 3 - Components (refactor)

* refactoring to create Component
* Edit: app/index.html
* Edit: app/app.js
* Edit: app/phone-list.component.js
* npm start
* http://localhost:8000/index.html

### 4 - Directory and File Organization

* Define the phoneList module (app/phone-list/phone-list.module.js)
* Register the phoneList component on the phoneList module (app/phone-list/phone-list.component.js)
* Define the phonecatApp module (app/app.module.js)
* Add a templateURL in phone-list.component.js
* Make sure to update index.html to all JS new scripts and delete app.js

### 5 - Filtering Repeaters

* Update Phone list component HTML template to add search box

### 6 - 2 Way Data Binding

* Update Phone list component HTML template
* Add "age" to Controller

### 7 - XHR & Dependency Injection

* create app/phones/phones.json
* update app/phone-list/phone-list.component.js for JSON

    $http.get('phones/phones.json').then(function(response) {
    self.phones = response.data;
    });

*  update app/phone-list/phone-list.component.js - inline annotation where, instead of just providing the function, you provide an array.
* added to html template to see JSON: <pre>{{$ctrl.phones | filter:$ctrl.query | orderBy:$ctrl.orderProp | json}}</pre>

### 8 - Templating links and images for the phones

* Add individual JSON phone files
* Link to phone files app/phone-list/phone-list.template.html
*


from original source tutorial:
https://docs.angularjs.org/tutorial
