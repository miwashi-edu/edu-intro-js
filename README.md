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
```

## service.js

```js

```

## ./\_\_tests\_\_/unittest.js

```js

```
