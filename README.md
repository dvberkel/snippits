snippits
========

> A jquery plugin that load snippits into textarea's

Usage
-----

Install snippits with [bower][] with the following command

```shell
bower install snippits
```

This will install `jquery.snippits.js` into the 'components/snippits'
directory. You can include it into you html page with the following
snippit.

```html
<script type='text/javascript' src='components/snippits/jquery.snippits.js'></script>
```

Afterwards it is possible to load snippits into textarea by first
selecting them with [jQuery][] and then calling `snippits()` on the
result set.

### Example

With the following html

```html
<textarea class='code' data-snippit='example.js'></textarea>
```

The following loads the `example.js` snippit from the `snippits` directory into the
above textarea

```javascript
$("textarea.code").snippits({
  suffix: 'snippit',
  directory: 'snippits',
  onFinish: function(){ /* do nothing */ }
});
```
### Options

The following options can be passed to the `snippits` call.

#### suffix

*default*: `snippit`

Controls the suffix to the data attribute that will be used to load a
snippit.

#### directory

*default*: 'snippits'

Specifies what directory to load the snippits from.

#### onFinish

*default*: function(){ /* do nothing */ }

A callback for when the snippits loading is finished.

[bower]: http://bower.io
[jQuery]: http://jquery.com/