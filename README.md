# request-query-utils

A package to isolate filters and sorts from a given request's query parameters

## Installation

```js
# using npm
npm install request-query-utils

# using yarn
yarn add request-query-utils
```

## Usage

```js
# using require
const { getRequestFilters, getRequestSorts, getRequestQueryParams } = require("request-query-utils");

# using import
import { getRequestFilters, getRequestSorts, getRequestQueryParams } from "request-query-utils";
```

## Example

```js
//isolate and put all request query params into an array
const params = getRequestQueryParams({
  req, // node.js request object
});

//isolate and put all request filter query params into an array
const filters = getRequestFilters({
  req, // node.js request object
});

//isolate and put all request sort query params into an array
const sorts = getRequestSorts({
  req, // node.js request object
});
```

## Additional Options

- All functions can take in an addition boolean parameter **returnObject** which will return a single object with the merged values isolated from the function. The return type by default is an array.
