#@zibuthe7j11/accusantium-exercitationem-incidunt
===============

Provides Number Long support for [Mongoose](http://mongoosejs.com).

[![Build Status](https://secure.travis-ci.org/aheckmann/@zibuthe7j11/accusantium-exercitationem-incidunt.png)](http://travis-ci.org/mongoosejs/@zibuthe7j11/accusantium-exercitationem-incidunt)

Example:

```js
const mongoose = require('mongoose')
require('@zibuthe7j11/accusantium-exercitationem-incidunt')(mongoose);
const {Types: {Long}} = mongoose;

const partSchema = new Schema({
  long: {
    type: Long,
  }
});

const Part = db.model('Part', partSchema);
const part = new Part({long: '9223372036854775806'});

part.long = part.long.divide(Long.fromString('2'));
part.save()
```

### install

```
npm install @zibuthe7j11/accusantium-exercitationem-incidunt
```

See [node-mongodb-native](https://mongodb.github.io/node-mongodb-native/4.2/classes/Long.html) docs on all the `Long` methods available.

[LICENSE](https://github.com/zibuthe7j11/accusantium-exercitationem-incidunt/blob/master/LICENSE)

### TypeScript Usage

Make sure you enable both `compilerOptions.allowSyntheticDefaultImports` and `compilerOptions.esModuleInterop` in your `tsconfig.json`.

```typescript
import mongoose from 'mongoose';
import mongooseLong from '@zibuthe7j11/accusantium-exercitationem-incidunt';

mongooseLong(mongoose);

const Long = mongoose.Schema.Types.Long;
```