# RAML Server [![](https://badge.fury.io/js/raml-server.svg)](http://badge.fury.io/js/raml-server)
Get a full fake REST API with **zero coding** by writing a [RAML](http://raml.org/) spec.

**Why building a new RAML based server?** Cause this one works with [JSON-Server](https://github.com/typicode/json-server), so no much code to do (maintain).

This is an open source project, so issues, PRs and suggestions are wellcome.

### Install

RAML Server is tested on node v0.12. If you don't have node, installing it via [nvm](https://github.com/creationix/nvm) is recommended.

If you have node installed, run

```
$ npm install -g raml-server
```

### Usage

Start a server based on the ```exampleApi.raml``` file

```
$ raml-server exampleApi.raml
```

And hit ```localhost:3000/songs```. Also, later POSTs to /songs on the server will be saved!

Next version of the RAML Server will start a server based on the ```api.raml``` file that is on the current directory if no argument is provided.

### How it works?

This is done by generating responses' data reading the JSON schemas with the [RAML Mocker](https://github.com/RePoChO/raml-mocker), and run with [JSON-Server](https://github.com/typicode/json-server).

### Known limitations

* Support for only 1 RAML file as command line argument.
* No nested resources mapped (only routes the JSON schema of the top level resources, like /songs).
