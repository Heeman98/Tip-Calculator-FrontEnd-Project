# Tip-Calculator-FrontEnd-Project
Tip Calculator made using HTML, CSS3 and Javascript.

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Calculate the correct tip and total cost of the bill per person

### Screenshot

![Project ScreenShot](https://github.com/FrolicBrat/Tip-Calculator-FrontEnd-Project/blob/82026791892a785403e01c86eb39a918826f107d/Img/Screenshot%202022-11-14%20at%2014-50-23%20Newton%20School%20Tip%20calculator%20JS%20Project.png)

### Links
- Live Site URL: [Netlify](https://tipcalculatorjsproject.netlify.app/)

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Mobile-first workflow

### What I learned

- Creation and design of regular expressions to truncate numbers with decimals. Interest rates are not rounded, they are generally truncated. To achieve this result we create a pattern and compare it with the result variable.

These expressions only work with strings, they are not allowed in numeric scopes. So, if the variable is numeric, it must first be transformed into a String field.

```js
const regex = /^\d+(\.\d{0,2})?/
}
```

Then we have:

- / 'pattern' / -> Regular expressions are enclosed in backslashes, so that it can be understood by the js
- ^ -> Tells the code to take the expression from the beginning of the string
- \ d + -> Indicates that 1 or more numeric digits are taken
- () -> The parentheses are used to generate a substring that groups the decimal section
- \. -> We indicate the decimal point
- \ d {0,2} -> Between braces we establish that the result is composed of 0-2 decimal digits -? -> We indicate in this way that the previous group is optional, matching 0 or 1 times

Finally, we convert the value of the numeric field into a string, and set the matcher according to the pattern:

```js
let tip = (facturar * valor) / usuario
let tipString = tip.toString().match(regex)[0].
