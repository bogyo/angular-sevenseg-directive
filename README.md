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
angular.module('myApp', ['ngSevenseg']);
```
Where You would like to place your seven-segment display you need to refer to it.
```html
  <sevenseg options="YourOptions"></sevenseg>
```
Or 
```html
  <span sevenseg  options="YourOptions"></span>
```

### Options
