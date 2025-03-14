# Welcome 🙋‍♂️ to JS Date 🏆

🙏 Please credit me if you use this or share it with others. 🙏

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

## Date in JavaScript

The `Date` object is used to work with dates and times in JavaScript.

### Creating Date Objects

There are four ways to create a new date object:

1. new Date()
2. new Date(year, month, day, hours, minutes, seconds, milliseconds)
3. new Date(milliseconds), milliseconds since 1970/01/01
4. new Date(date string)

```javascript
// Create a new date object
let date = new Date();
console.log(date); // current date and time

// Create a new date object with a specific date and time
let date = new Date(2021, 0, 1, 12, 0, 0, 0);
console.log(date); // Fri Jan 01 2021 12:00:00 GMT+0000 (Coordinated Universal Time)

// Create a new date object with milliseconds
let date = new Date(1609459200000);
console.log(date); // Fri Jan 01 2021 00:00:00 GMT+0000 (Coordinated Universal Time)

// Create a new date object with a date string
let date = new Date("2021-01-01T12:00:00Z");
console.log(date); // Fri Jan 01 2021 12:00:00 GMT+0000 (Coordinated Universal Time)
```

### Date Methods

The `Date` object has a number of methods for working with dates and times.

```javascript
let date = new Date();
date.getFullYear(); // get the year
date.getMonth(); // get the month (0-11) - January is 0 IMPORTANT
date.getDate(); // get the day of the month (1-31)
date.getDay(); // get the day of the week (0-6) - Sunday is 0
date.getHours(); // get the hour (0-23)
date.getMinutes(); // get the minutes (0-59)
date.getSeconds(); // get the seconds (0-59)
date.getMilliseconds(); // get the milliseconds (0-999)
date.getTime(); // get the milliseconds since 1970/01/01
date.toString(); // get the date as a string
```

### Date Formats

JavaScript does not have a built-in date format function. However, you can create your own date format function using the `Date` object methods.

```javascript
function formatDate(date) {
  let year = date.getFullYear();
  let month = date.getMonth() + 1;
  let day = date.getDate();

  if (month < 10) {
    month = "0" + month;
  }

  if (day < 10) {
    day = "0" + day;
  }

  return year + "-" + month + "-" + day;
}

let date = new Date();
console.log(formatDate(date)); // 2021-01-01

// You can also use the toISOString() method to get the date in ISO format
date.toISOString(); // 2021-01-01T12:00:00.000Z

// You can also use the toUTCString() method to get the date in UTC format
date.toUTCString(); // Fri, 01 Jan 2021 12:00:00 GMT

// You can also use the toDateString() method to get the date in a readable format
date.toDateString(); // Fri Jan 01 2021

// You can also use the toTimeString() method to get the time in a readable format
date.toTimeString(); // 12:00:00 GMT+0000 (Coordinated Universal Time)

// You can also use the toLocaleDateString() method to get the date in a locale format
date.toLocaleDateString(); // 1/1/2021

// You can also use the toLocaleTimeString() method to get the time in a locale format
date.toLocaleTimeString(); // 12:00:00 PM

// You can also use the toLocaleString() method to get the date and time in a locale format
date.toLocaleString(); // 1/1/2021, 12:00:00 PM
```

Passing the date format as an argument to the `toLocaleString()` method.

```javascript
let date = new Date();
date.toLocaleString("en-US", { dateStyle: "full", timeStyle: "long" }); // Friday, January 1, 2021 at 12:00:00 PM GMT+00:00
date.toLocaleString("en-US", { dateStyle: "full", timeStyle: "short" }); // Friday, January 1, 2021 at 12:00 PM
date.toLocaleString("en-US", { dateStyle: "medium", timeStyle: "short" }); // Jan 1, 2021, 12:00 PM
date.toLocaleString("en-US", { dateStyle: "short", timeStyle: "short" }); // 1/1/2021, 12:00 PM
```

Passing the date format as 'YYYY-MM-DD' to the `toLocaleString()` method.

```javascript
let date = new Date();
date.toLocaleString("en-US", { year: "numeric", month: "2-digit", day: "2-digit" }); // 01/01/2021

const date = new Date();
const formattedDate = date.toISOString().split('T')[0];
console.log(formattedDate); // Outputs: 'YYYY-MM-DD'
```

### Comparing Dates

You can compare dates using the comparison operators.

```javascript
let date1 = new Date("2021-01-01");
let date2 = new Date("2021-01-02");
date1 < date2; // true
date1 > date2; // false
date1 == date2; // false
```

### Date Arithmetic

You can perform arithmetic operations on dates using the `Date` object methods.

```javascript
let date = new Date();
date.setDate(date.getDate() + 7); // add 7 days
date.setMonth(date.getMonth() + 1); // add 1 month
date.setFullYear(date.getFullYear() + 1); // add 1 year

let date1 = new Date("2021-01-01");
let date2 = new Date("2021-01-02");
let diff = date2 - date1; // difference in milliseconds
```

### [ ⏭ Next: Arrays in JS](./11_arrays.md)

### [🔙 Back To JS Readme](./js.md)

### [🔙 Back To Main Readme](../../../README.md)

🙏 Please credit me if you use this or share it with others. 🙏

