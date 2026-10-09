<p align="center">
    <a href="https://github.com/inikulin/parse5">
        <img src="https://raw.github.com/inikulin/parse5/master/media/logo.png" alt="parse5" />
    </a>
</p>

<div align="center">
<h1>parse5-plain-text-conversion-stream</h1>
<i><b>Stream that converts plain text into HTML document as required by <a href="https://html.spec.whatwg.org/#read-text">HTML specification</a>.</b></i>
</div>
<br>

<div align="center">
<code>npm install --save parse5 parse5-plain-text-conversion-stream</code>
</div>
<br>

## Usage

`PlainTextConversionStream` accepts plain text and produces an HTML document with the text inside a `<pre>` element. It does not parse an HTML input stream. This example also serializes the result with `parse5`:

```js
import { finished } from 'node:stream/promises';
import { serialize } from 'parse5';
import { PlainTextConversionStream } from 'parse5-plain-text-conversion-stream';

const converter = new PlainTextConversionStream();
converter.end('Hello, world!');
await finished(converter);

console.log(serialize(converter.document));
```

<p align="center">
  📖 <a href="https://parse5.js.org/modules/parse5-plain-text-conversion-stream.html"><b>Documentation</b></a> 📖
</p>

---

<p align="center">
  <a href="https://github.com/inikulin/parse5/tree/master/docs/list-of-packages.md">List of parse5 toolset packages</a>
</p>

<p align="center">
    <a href="https://github.com/inikulin/parse5">GitHub</a>
</p>

<p align="center">
    <a href="https://github.com/inikulin/parse5/releases">Changelog</a>
</p>
