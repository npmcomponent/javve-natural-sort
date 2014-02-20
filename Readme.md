*This repository is a mirror of the [component](http://component.io) module [javve/natural-sort](http://github.com/javve/natural-sort). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/javve-natural-sort`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
![web component logo](http://i49.tinypic.com/e7nj9v.png)

# Natural sort algorithm with unicode support

The algorithm is written by [Jim Palmer](http://www.linkedin.com/in/jimbob)
and found at [http://www.overset.com/2008/09/01/javascript-natural-sort-algorithm/](http://www.overset.com/2008/09/01/javascript-natural-sort-algorithm/).

I, [javve](http://github.com/javve), only put it into a Component.

## Installation

    $ component install javve/natural-sort

## Example

```js
var naturalSort = require('natural-sort');

var values = ['B', 'a', 'D', 'c'];

values.sort(naturalSort); // ['B', 'D', 'a', 'c']

values.sort(function(a, b) {
    return naturalSort(a, b, { insensitive: true });
}); // ['a', 'B', 'c', 'D']

values.sort(function(a, b) {
    return naturalSort(a, b, { insensitive: true, desc: true })
}); // ['D', 'c', 'B', 'a']


var values = [
    { val: 'B' },
    { val: 'a' },
    { val: 'D' },
    { val: 'c' }
];

values.sort(function(a, b) {
    return naturalSort(a.val, b.val, { insensitive: true });
}); // ['a', 'B', 'c', 'D']

```

Find more examples at [http://www.overset.com/2008/09/01/javascript-natural-sort-algorithm/](http://www.overset.com/2008/09/01/javascript-natural-sort-algorithm/)
or look at the tests in `/test`. It's quite impressive. Handles dates, etc.

## License

MIT
