# Serverless Plugin: Support Tagging API Gateway Stages

[![Build Status](https://travis-ci.org/silvermine/serverless-plugin-apigateway-stage-tags.svg?branch=master)](https://travis-ci.org/silvermine/serverless-plugin-apigateway-stage-tags)
[![Coverage Status](https://coveralls.io/repos/github/silvermine/serverless-plugin-apigateway-stage-tags/badge.svg?branch=master)](https://coveralls.io/github/silvermine/serverless-plugin-apigateway-stage-tags?branch=master)
[![Dependency Status](https://david-dm.org/silvermine/serverless-plugin-apigateway-stage-tags.svg)](https://david-dm.org/silvermine/serverless-plugin-apigateway-stage-tags)
[![Dev Dependency Status](https://david-dm.org/silvermine/serverless-plugin-apigateway-stage-tags/dev-status.svg)](https://david-dm.org/silvermine/serverless-plugin-apigateway-stage-tags#info=devDependencies&view=table)


## What is it?

This is a plugin for the Serverless framework that adds support for setting tags on an API
Gateway stage.

Normally CloudFormation supports tagging for resources created by a CloudFormation
template. Unfortunately, API Gateway stages are not one of those resources. AWS does
provided support for tagging via the [AWS Console][tagging-via-console],
[aws-cli][tagging-via-cli], and the [API Gateway REST API][tagging-via-api]. This plugin
uses this support to automate the creation of the tags for the API Gateway stages in the
service.

This plugin will mimic the stack tag propagation that
[CloudFormation automatically performs][automatic-stack-tags]. There is not currently
support for adding additional tags to a API Gateway stage. If this is a feature you need,
[feel free to submit a PR](#how-do-i-contribute)!

Once CloudFormation supports adding tags to an API Gateway stage and
serverless/serverless#4644 is completed, this plugin will be obsolete.

## How do I use it?

There are two steps:

### Install the Plugin as a Development Dependency

```bash
npm install --save-dev --save-exact serverless-plugin-apigateway-stage-tags
```

### Telling Serverless to Use the Plugin

Simply add this plugin to the list of plugins in your `serverless.yml` file:

```yml
plugins:
   - serverless-plugin-apigateway-stage-tags
```


## How do I contribute?

We genuinely appreciate external contributions. See [our extensive
documentation][contributing] on how to contribute.


## License

This software is released under the MIT license. See [the license file](LICENSE) for more
details.


[tagging-via-console]: https://docs.aws.amazon.com/apigateway/latest/developerguide/set-up-tags.html#set-up-tags-using-console
[tagging-via-cli]: https://docs.aws.amazon.com/cli/latest/reference/apigateway/tag-resource.html
[tagging-via-api]: https://docs.aws.amazon.com/apigateway/latest/developerguide/set-up-tags.html#set-up-tags-using-api
[automatic-stack-tags]: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html
[contributing]: https://github.com/silvermine/silvermine-info#contributing
