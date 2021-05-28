# stc-json-rpc

`json-rpc-engine` middleware for starcoin's REST endpoints.

### usage as provider

```js
const createInfuraProvider = require('stc-json-rpc/src/createProvider')
const Ethjs = require('ethjs')

const provider = createInfuraProvider({ network: 'main', projectId: 'example' })
const eth = new Ethjs(provider)
```

### usage as middleware

```js
const createInfuraMiddleware = require('stc-json-rpc')
const RpcEngine = require('json-rpc-engine')

const engine = new RpcEngine()
engine.push(createInfuraMiddleware({ network: 'barnard', projectId: 'example' }))
```

## Running Tests

```bash
yarn test
```
