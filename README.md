# Robintrack API

Unofficial node.js client for accessing the APIs called on Robintrack.net.

## Installation

```sh
npm i -S @joemccann/robintrack-api
```

## Usage

```js
const rta = require('@joemccann/robintrack-api')

const params = {
  method: 'largest_popularity_increases',
  options: {
    hours_ago: 48,
    limit: 50,
    percentage: true,
    min_popularity: 50,
    start_index: 0
  }
}

try {
	const { data = [], statusCode = 0 } = await rta(params)
	console.dir(data) // [...]
	console.log(statusCode) // 200
}
catch(e){
	console.error(e)
}
```

## Tests

```sh
npm i -D
npm test
```

## License

MIT

## Authors

- [Joe McCann](https://twitter.com/joemccann)
