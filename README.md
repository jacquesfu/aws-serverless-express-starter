# Serverless Framework Node Express API on AWS

This is a starter template is for quickly starting a boilerplate for Express that is ready to deploy on AWS. This version is largely based on the example generated by the `serverless` command but removes a few more steps such as pre-installing serverless offline.

## Usage

### Quick Start

Install dependencies with:

```
npm install
```

Run locally with:

```
npm run dev
```

### Deployment

Deploy with:

```
serverless deploy
```

After running deploy, you can visit the URL listed:

```bash
endpoints:
  ANY - https://xxxxxxx.execute-api.us-east-1.amazonaws.com/
functions:
  api: aws-node-express-api-dev-api
layers:
  None
```

## Anatomy of the template

This template configures a single function, `api`, which is responsible for handling all incoming requests thanks to the `httpApi` event. To learn more about `httpApi` event configuration options, please refer to [httpApi event docs](https://www.serverless.com/framework/docs/providers/aws/events/http-api/). As the event is configured in a way to accept all incoming requests, `express` framework is responsible for routing and handling requests internally. Implementation takes advantage of `serverless-http` package, which allows you to wrap existing `express` applications. To learn more about `serverless-http`, please refer to corresponding [GitHub repository](https://github.com/dougmoscrop/serverless-http).

To learn more about the capabilities of `serverless-offline`, please refer to its [GitHub repository](https://github.com/dherault/serverless-offline).

### Creating this template

- Generated this example using `serverless` command and selecting `Express API`
- Installed serverless using `serverless plugin install -n serverless-offline`
- Added `serverless-offline` to `dev` script
