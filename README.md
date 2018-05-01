# testcafe-reporter-phil
[![Build Status](https://travis-ci.org/FreakyTurtle/testcafe-reporter-phil.svg)](https://travis-ci.org/FreakyTurtle/testcafe-reporter-phil)

This is the **phil** reporter plugin for [TestCafe](http://devexpress.github.io/testcafe).

Phil outputs a semi-styled html report to help track documentation and for use in wiki tools like confluence.

Why is it called phil? As an homage to Bill Murray's reporter character in the film groundhog day.

<p align="center">
    <img src="https://github.com/FreakyTurtle/tescafe-reporter-phil/blob/master/media/preview.png" alt="preview" />
</p>

## Install

```
npm install testcafe-reporter-phil
```

## Usage

When you run tests from the command line, specify the reporter name by using the `--reporter` option:

```
testcafe chrome 'path/to/test/file.js' --reporter phil
```


When you use API, pass the reporter name to the `reporter()` method:

```js
testCafe
    .createRunner()
    .src('path/to/test/file.js')
    .browsers('chrome')
    .reporter('phil') // <-
    .run();
```

Although we recommend setting up a custom stream to output to within the  `reporter()` method:

```js
const fs = require('fs');
const stream = fs.createWriteStream(__dirname+'/reports/' + new Date().getTime() + '.html')

testCafe
    .createRunner()
    .src('path/to/test/file.js')
    .browsers('chrome')
    .reporter('phil', stream) // <-
    .run();
```

## Author
FreakyTurtle (http://www.freakyturtle.com)
