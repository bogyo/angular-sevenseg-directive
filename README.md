# angular-sevenseg-directive

Angular directive for seven-segment display.
No jQuery dependency needed.

### Overview
- All graphics are SVG => free scaling
- single or multiple digits to display
- two-way data binding is avaliable
- options for changing colors, number of digits, decimal point to display

### Default usage
There is assuming that You already have a script for angular.js in your html head section.
You need to add the following code snippet to your html head section as well

```html
<script type="text/javascript" src="ng-sevenseg.js"></script>
```

And register the seven-segment display directive in your application module:

```javascript
angular.module('yourApp', ['ngSevenseg']);
```
Where You would like to place your seven-segment display you need to refer to it. E.g.:
```html
  <sevenseg options="yourOptions"></sevenseg>
```
or with html tag You can use other elements too (like span, p)
```html
  <div sevenseg  options="yourOptions"></div>
```

### Options

You need to specify your options in an object in your module. You need to set up at least the value and the number of digits which You would like to display.

```javascript
 $scope.yourOptions = {
    digits: 2,
    value: 46
  };
```
You have opportunity to customise other properties. It is not necessary, the directive will use its default settings if You do not overwrite them. Possibilities: 

```javascript
 $scope.yourOptions = {
    digits: 2,
    value: 46,
    
  };
```
### Data binding
If you would like to display dynamic numbers instead of static.
In your view:
```html
  <sevenseg options="yourOptions" data="yourValue"></sevenseg>
```
In your controller: 
```javascript
  $scope.yourValue = "5";
  
  $scope.yourOptions = {
    digits: 1
  };
```
If the value based on a user input, add to your view file the following:
```html
<input ng-model="yourValue" type="text"></input>
```
