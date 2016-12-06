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


from original source tutorial:
https://docs.angularjs.org/tutorial
