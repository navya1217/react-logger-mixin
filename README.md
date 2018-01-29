
## Install

```
npm install react-logger --save
```
## Usage

This module exposes `console.log` `console.error` and `console.dir` on the component. Everything is what you would normally expect, but log messages are prefixed with the displayName of the component so you know where things are coming from. This also works cross-browser, so on browsers without the console object it won't blow up.

```js
var React = require('react');
var LoggerMixin = require('react-logger');

React.createClass({
  displayName: 'TestComponent',
  // Add mixin
  mixins: [LoggerMixin],
  componentDidMount: function() {
    // Log: [TestComponent] something insightful
    this.log('something insightful');
  },
  render: function() {
    // do stuff here
  }
});
```
