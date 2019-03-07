### mb-swagger-ui
mb-swagger-ui is an node express middleware to show swagger-ui 3 for your local (or external) api.

# FORK FROM : https://github.com/pgroot/express-swagger-generator

Modified to support a basepath specification. Author did not respond to merge request for 5 months hence the fork.

#### Installation

```
npm install --save mb-swagger-ui
```

#### Usage

```
const express   = require('express');
const app       = express();
const swaggerUi = require('mb-swagger-ui');

app.use('/api-docs.json', function (req, res) {
  res.json(require('./path/to/swaggerize/docs.json'));
});
app.use('/api-docs', swaggerUi());

app.listen(3000);

```

#### Generate swagger doc.json

[mb-swagger-gen](https://github.com/Lorune/mb-swagger-gen)