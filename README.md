# react-simple-date-picker

A simple, modular React date picker component


![react-simple-date-picker](https://andrewware.xyz/img/react-simple-date-picker.gif)


## Installation
The package can be installed via NPM:
```
npm i -S react-simple-date-picker
```

You'll also need to install the React PropTypes library if you haven't already.
```
npm i -S prop-types
```


## Usage
```js
import React from 'react';
import DatePicker from 'react-simple-date-picker';

const MyForm = () => (
  <form className="MyForm" onSubmit={(e) => {
    const dateInput = e.target.querySelectorAll('input[name$="date"]')[0];
    // dateInput.value is formatted as a YYYY-MM-DD string by default
    doSomething(dateInput.value);
  }}>
    <DatePicker />
    <button type="submit">Submit</button>
  </form>
);

export default MyForm;
```


## Customization
This DatePicker component is built simple on purpose. It's intended to be built upon. However, there are some pieces that are customizable right out of the box.

These customizable props include:
- `dirty`: should the currently selected date be shown (highlighted cell) [defaults to `true`]
- `inputName`: the html input element's "name" property [defaults to `'date'`]
- `showDateReset`: show the reset button [defaults to `true`]
- `showDateSelected`: show the currently selected date in a human readable string [defaults to `true`]
- `showWeekDayName`: show the abbreviated week names at the top of the calendar [defaults to `true`]
- `showMonthChangeButtons`: show the left/right arrow buttons for changing the month [defaults to `true`]
- `showYearChangeButtons`: show the up/down arrow buttons for changing the year [defaults to `true`]
- `initialDate`: the initially selected date (Date) [defaults to `new Date()`]


### Usage With Custom Props
```js
  ...
  <DatePicker
    inputName="MyForm_date"
    showDateReset=false
    showDateSelected=false
    initialDate={new Date('2021-01-20')}
  />
  ...
```


### Continuous Development
If you wish to build upon or style upon the existing component, checkout the [dev branch](https://github.com/andrew-ware/react-simple-date-picker/tree/dev) for precompiled sass files.
