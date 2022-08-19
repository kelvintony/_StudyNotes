```javascript
//
//
===> index.js
const os = require('os');
const path = require('path');

console.log('first print');
console.log(os.type());
console.log(os.version());
console.log(os.homedir());

console.log('\nsecond print');
console.log(__filename);
console.log(__dirname);

console.log('\nthird print');
console.log(path.dirname(__filename));
console.log(path.basename(__filename));
console.log(path.extname(__filename));

console.log('\nfouth print');
console.log(path.parse(__filename));

    :console output:

        first print
        Windows_NT
        Windows 10 Pro
        C:\Users\HP PC

        second print
        C:\Users\HP PC\Desktop\Projects\blog-project\backend\index.js      
        C:\Users\HP PC\Desktop\Projects\blog-project\backend

        third print
        C:\Users\HP PC\Desktop\Projects\blog-project\backend
        index.js
        .js

        fouth print
        {
        root: 'C:\\',
        dir: 'C:\\Users\\HP PC\\Desktop\\Projects\\blog-project\\backend',
        base: 'index.js',
        ext: '.js',
        name: 'index'
        }


