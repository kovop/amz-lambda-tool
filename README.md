# Servie Lambda

> Servie transport for AWS lambda proxy.

## Installation

```
npm install amz-lambda-tool --save
```

## Usage

Wrap a standard Servie middleware function in `createHandler` to return a AWS Lambda handler.

```ts
import { createHandler } from "servie-lambda";
import { compose } from "throwback";
import { get } from "servie-route";

export const handler = createHandler(
  compose([get("/test", req => new Response("hello world"))])
);
```

## TypeScript

This project is written using [TypeScript](https://github.com/Microsoft/TypeScript) and publishes the definitions directly to NPM.

## License

Apache 2.0
