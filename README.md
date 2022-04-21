# Weasyprint Wrapper

A fixed node wrapper module for use with the weasyprint Python package.

This module is a fork of [repo](https://github.com/dills122/weasyprint-wrapper) with minor updates and reuploaded back to npm.


Install the package (Python3 required):
```
pip3 install weasyprint
```

Add the NodeJS wrapper to your project:
```
npm i weasyprint
```

Example usage:

```javascript
const weasyprint = require('weasyprint-wrapper');

// Optionnal: specify the location of weasyprint cli if not in PATH
weasyprint.command = ;

// URL, specifying the format & default command to spawn weasyprint
const resBuffer = await weasyprint('http://google.com/', { 
    command: '~/programs/weasyprint',
    pageSize: 'letter'
});
  
// HTML
const resbuffer = await weasyprint('<h1>Test</h1><p>Hello world</p>');

// Save in a file
try {
    const buffer = await weasyprint('<h1>Test</h1><p>Hello world</p>');
    fs.writeFileSync('test.pdf', buffer);
} catch (err) {
    console.error(err);
}
```
