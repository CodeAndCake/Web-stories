
Using [Mousetrap](https://github.com/ccampbell/mousetrap) to capture keyboard events and make the story *makey-makey-able*.

Need to turn off AMD and node.js stuff at the end of the library file, like so

```js
/*    // expose as a common js module
    if (typeof module !== 'undefined' && module.exports) {
        module.exports = Mousetrap;
    }

    // expose mousetrap as an AMD module
    if (typeof define === 'function' && define.amd) {
        define(function() {
            return Mousetrap;
        });
    }*/
}) (window, document);
```