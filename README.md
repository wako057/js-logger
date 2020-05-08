# cpm-logger
Wrapper for [node-bunyan](https://github.com/trentm/node-bunyan).

## Usage

### Initialization
```javascript
const logger = require("js-logger").init(configJSON);
```

### Configuration

#### JSON Configuration
cpm-logger takes in parameter the following JSON :

```JSON
{
     "name" : "mylogname",
     "files" : {
         "enable" : true,
         "path" : "/path/to/log",
         "name" : "indb",
         "level" : "loglevel"
     }
 }
```

#### Log level
  * [Bunyan levels](https://github.com/trentm/node-bunyan#log-method-api)

#### Console (output)
If you want log on console, `NODE_ENV` (system env) should be set to `development`. Use bunyan cli in order to formatting output example :
```bash
node myapp.js | bunyan
```
Use option `-o` to change format. More information `bunyan --help`.

Log level is managed throught `ENV_LOG_LEVEL`.

#### Test syntax

```bash
$ npm run tests:syntax -s
```
