# testcafe-reporter-phil
[![Build Status](https://travis-ci.org/FreakyTurtle/testcafe-reporter-phil.svg)](https://travis-ci.org/FreakyTurtle/testcafe-reporter-phil)

This is the **phil** reporter plugin for [TestCafe](http://devexpress.github.io/testcafe).

<p align="center">
    <img src="https://raw.github.com/FreakyTurtle/testcafe-reporter-phil/master/media/preview.png" alt="preview" />
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

## Author
James (http://freakyturtle.com)
