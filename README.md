# mongoose-detective [![Build Status](https://travis-ci.org/Zertz/mongoose-detective.png)](https://travis-ci.org/Zertz/mongoose-detective) [![NPM version](https://badge.fury.io/js/mongoose-detective.png)](http://badge.fury.io/js/mongoose-detective)

Find the referenced model name at a specified path

```js
npm i mongoose-detective --save
```

## Usage

```js
const detective = require('mongoose-detective')
const mongoose = require('mongoose')

const InvoiceSchema = new Schema({
  customer: { type: mongoose.Schema.Types.ObjectId, ref: 'Customer' }
})

mongoose.model('Invoice', InvoiceSchema)

let modelName = detective(mongoose.models.Invoice, 'customer')

// modelName = 'Customer'
```

## Contributing

I'd love for you to contribute and make mongoose-detective even better than it is today!

### Getting started

```
git clone https://github.com/Zertz/mongoose-detective.git
npm install
npm test
```

### Guidelines

- [Standard](https://github.com/feross/standard) style
- Use ES2015 features when appropriate
