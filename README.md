CSON-js
-------
__CSON__(Cursive Script Object Notation)
is a superset of [JSON](http://json.org/)
that can be written by hand and translated to a canonical JSON.

[CSON](http://noe.mearie.org/cson/) is
designed by [Kang Seonghoon](https://github.com/lifthrasiir),
and CSON-js is written by [JongChan Choi](https://github.com/disjukr).

Please check out the [demo](http://0xabcdef.com/CSON-js/)


Usage
-----

```javascript
CSON.toJSON('"a": 1, b = 2');
// returns {"a":1,"b":2} as string

CSON.parse('c: |verbatim\n|string!\n "d" = ["newline"\n"to"\n"separate"]');
// returns {"c": "verbatim\nstring!", "d": ["newline", "to", "separate"]} as object
```

you can make formatted json output from cson:

```javascript
CSON.toJSON('e = {}, f = [1, 2, 3]', 4/* indent by four spaces */);
```

that returns

```json
{
    "e": {},
    "f": [
        1,
        2,
        3
    ]
}
```

`CSON.toJSON` returns minified json if you putting `0`(or any kind of false value) to `indent` parameter.
this is default.

if you want formatted json without indentation, use `'0'` instead of `0`:

```javascript
CSON.toJSON('e = {}, f = [1, 2, 3]', '0');
```

returns

```json
{
"e": {},
"f": [
1,
2,
3
]
}
```


License
-------

The MIT License (MIT)

Copyright (c) 2013, JongChan Choi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.