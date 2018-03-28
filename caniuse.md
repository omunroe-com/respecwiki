
Adds a [Can I Use](http://caniuse.com) support table in header (before the copyright message). [(Preview)](https://i.imgur.com/WEqFraF.png)

# This documents an unreleased feature.

## Example:

``` js
// basic example
var respecConfig = {
  caniuse: "payment-request",
};
```

``` js
// example with configuration (see options below)
var respecConfig = {
  caniuse: {
    feature: "payment-request",
    browsers: ["chrome", "safari"],
  },
};
```

## Configuration Options: 

<dl>

<dt><code>feature</code></dt>
<dd>(required) Can I Use feature key</dd>

<dt><code>browsers</code></dt>
<dd>Array of browsers to show support for. <br>
Default: <code>["chrome", "firefox", "safari", "edge"]</code><br>
Supported Values: 
<ul>
	<li><code>chrome</code> -- Chrome</li>
	<li><code>firefox</code> -- Firefox</li>
	<li><code>ie</code> -- IE</li>
	<li><code>edge</code> -- Edge</li>
	<li><code>android</code> -- Android</li>
	<li><code>safari</code> -- Safari</li>
	<li><code>opera</code> -- Opera</li>
	<li><code>bb</code> -- Blackberry</li>
	<li><code>and_uc</code> -- UC (Android)</li>
	<li><code>and_ff</code> -- Firefox (Android)</li></ul>
</dd>

<dt><code>versions</code></dt>
<dd>Number of browser versions to show<br>
Default: <code>4</code></dd>

<dt><code>maxAge</code></dt>
<dd>Cache duration (in ms). <br>
Set to <code>0</code> to get fresh data each on each request.<br>
Default: <code>86400000</code>  // 24 hours</dd>

<dt><code>apiURL</code></dt>
<dd>(For testing) Use a custom URL that returns a JSON response with <code>stats</code> key as the browser data object.<br>
Use <code>{FEATURE}</code> as placeholder in URL to replace it by a value of <code>caniuse.feature</code></dd>
</dl>