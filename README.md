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

## Förklaringar

### cd ~

> Du sätter din hemkatalog som arbetskatalog (du går till din hemkatalog)

### cd ws

> Undersförstått att du har en katalog som heter ws i din hemkatalog så sätter du nu den som arbetskatalog. (Du går till ditt workspace)

### rm -rf edu-intro-js

> Du tar bort ett tidigare försök att skapa projektet. 
> rm betyder remove.
> rm kan inte ta bort kataloger, så vi använder växeln -r för att gå ned i kataloger och växeln -f för att slippa svara ja på om vi är säkra på att vi vill ta bort filer.

### mkdir edu-intro-js

> Make DIrectory, vi skapar katalogen edu-intro-js

### cd edu-intro-js

> Vi sätter edu-intro-js till arbetskatalog (vi går in till projektet)

### touch service.js

> Vi skapar filen service.js. (Egentligen betyder touch att vi sätter senast ändrad datum på filen till nu, men om inte filen finns så skapas den.)

### mkdir __tests__

> Vi skapar en katalog som ofta är standard i node projekt. Testramverket jest kommer automatiskt att leta efter test i denna katalog.

### touch ./__tests__/unitest.js

> Vi skapar en javascript fil där vi kan skriva test.

### npm init -y

> vi gör ett node projekt av katalogen. Egentligen skapar vi bara en fil som heter package.json som innehåller samtliga instruktioner för hur vår kod kommer att köras.

### npm pkg

> Vi redigerar package.json.

### npm install -D jest

> Vi installerar installerar ramverket jest. -D (eller --save-dev lägger in det som utvecklingsmiljö)

## vi

> Vi startar vår text editor och redigerar service.js och unittest.js
