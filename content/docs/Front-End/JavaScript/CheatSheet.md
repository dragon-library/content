---
weight: 1
bookFlatSection: true
title: JavaScript Cheat Sheet
bookToc: true
---

JavaScript Cheat Sheet
====

- [*Link*](https://htmlcheatsheet.com/js/?fbclid=IwAR3TcjRcgtrQMoJC2dup8OFFPNy2up7l2-HKoU__JUB8TYLDDa5nX_Sgcrc)

## If - Else⇵

```js
if ((age >= 14) && (age < 19)) {        // logical condition
    status = "Eligible.";               // executed if condition is true
} else {                                // else block is optional
    status = "Not eligible.";           // executed if condition is false
}
Switch Statement
switch (new Date().getDay()) {      // input is current day
    case 6:                         // if (day == 6)
        text = "Saturday";          
        break;
    case 0:                         // if (day == 0)
        text = "Sunday";
        break;
    default:                        // else...
        text = "Whatever";
} 
```

Basics➤

## On page script
```js
<script type="text/javascript">
</script>
Include external JS file
<script src="filename.js"></script>
```
Delay - 1 second timeout

```js
setTimeout(function () {	
}, 1000);
Functions
function addNumbers(a, b) {
    return a + b; ;
}
x = addNumbers(1, 2);
Edit DOM element
document.getElementById("elementID").innerHTML = "Hello World!";
```
Output

```
console.log(a);             // write to the browser console
document.write(a);          // write to the HTML
alert(a);                   // output in an alert box
confirm("Really?");         // yes/no dialog, returns true/false depending on user click
prompt("Your age?","0");    // input dialog. Second argument is the initial value
Comments
/* Multi line
   comment */
// One line

```