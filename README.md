# json-markup

Prettyprint JSON to HTML

It is available through npm

	npm install json-markup

json-markup will take a JSON document and add markup to it so it can be styled in a browser.

``` js
require.config({
    paths: {
        jsonMarkup: '../node_modules/json-markup/index'
    },
    shim: {
        jsonMarkup: {
            exports: 'jsonmarkup'
        }
    }
});

var jsonMarkup = require('jsonMarkup');

var html = jsonMarkup({hello:'world'});

console.log(html);
```

The above example will print the following HTML

``` html
<div class="json-markup">{
	<span class="json-markup-key">hello:</span> <span class="json-markup-string">"world"</span>
}</div>
```

Afterwards you can use css to style your output to your liking.
A stylesheet similar to [JSON view](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc) is included in [style.css](https://github.com/mafintosh/json-markup/blob/master/style.css)
