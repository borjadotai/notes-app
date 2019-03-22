#### Steps

To support the different chapters and steps of the tutorial; we use branches to represent the project codebase at the various points. Here is an index of the various chapters and branches in order.

- [Set up the Serverless Framework](../../tree/setup-the-serverless-framework)
- [Add Support for ES6/ES7 JavaScript](../../tree/add-support-for-es6-es7-javascript)
- [Add a Create Note API](../../tree/add-a-create-note-api)
- [Add a Get Note API](../../tree/add-a-get-note-api)
- [Add a List All the Notes API](../../tree/add-a-list-all-the-notes-api)
- [Add an Update Note API](../../tree/add-an-update-note-api)
- [Add a Delete Note API](../../tree/add-a-delete-note-api)
- [Unit Tests in Serverless](../../tree/unit-tests-in-serverless)

#### Usage

To use this repo locally you need to have the [Serverless framework](https://serverless.com) installed.

``` bash
$ npm install serverless -g
```

Clone this repo and install the NPM packages.

``` bash
$ git clone https://github.com/AnomalyInnovations/serverless-stack-demo-api
$ npm install
```

Run a single API on local.

``` bash
$ serverless invoke local --function list --path event.json
```

Where, `event.json` contains the request event info and looks something like this.

``` json
{
  "requestContext": {
    "authorizer": {
      "claims": {
        "sub": "USER-SUB-1234"
      }
    }
  }
}
```

Finally, run this to deploy to your AWS account.

``` bash
$ serverless deploy
```
