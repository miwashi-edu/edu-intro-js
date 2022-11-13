# edu-intro-js

> En enkel introduktion till nodejs projekt.

## Instruktioner

```bash
cd ~
cd ws
rm -rf edu-intro-js #Försiktig med denna
mkdir edu-intro-js
cd edu-intro-js
touch service.js
mkdir __tests__
touch ./__tests__/unitest.js
npm init -y
npm pkg set main="service.js"
npm pkg set scripts.start="node service.js" 
npm pkg set scripts.dev="nodemon service.js" 
npm pkg set scripts.test="jest"
npm install -D nodemon
npm install -D jest
vi service.js # Skriv in kod under rubriken service.js
vi ./__tests__/unittest.js # Skriv in kod under rubriken unittest.js

npm test # Testa din kod
npm start # Kör din kod
```

## service.js

```js
console.log(sum(2,3));

function sum(a, b) {
  return a + b;
}
module.exports = sum;
```
 
## unittest.js

```js
const sum = require('../service.js');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

## package.json

> Gör du allting rätt ska din package.json se ut som detta.

```json
{
  "name": "edu-intro",
  "version": "1.0.0",
  "description": "",
  "main": "service.js",
  "scripts": {
    "test": "jest",
    "dev": "node service.js",
    "start": "node service.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "jest": "^29.3.1",
    "nodemon": "^2.0.20"
  }
}
```
