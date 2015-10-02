---
title: Partner Documentation
---

# Partner Documentation

*This documentation is currently being updated and improved. It will eventually become the single place to go for Partners to find all steps required to onboard, build a tile and release new versions. If you feel there is any content missing or have any feedback please provide this to pcf-feedback@pivotal.io*

# Building your product for the Pivotal Cloud Foundry Platform

There are several steps to building a product for the PCF Platform.

## BOSH Release

Visit the [BOSH Documentation Website](www.bosh.io), in particular the [creating a release guide](http://bosh.io/docs/create-release.html).

You can also refer to the [Redis](https://github.com/pivotal-cf/cf-redis-release) and [RabbitMQ](https://github.com/pivotal-cf/cf-rabbitmq-release) open source releases for example implementations.

## OpsManager tile

To be able to deploy the BOSH release you have created through Pivotal OpsManager, you need to build what is referred to as a tile.

This requires you to write some metadata which explains how the UI in OpsManager should be laid out and how the product should be deployed.

Visit the [OpsManager documentation](http://docs.pivotal.io/pivotalcf/packaging/index.html) for more details and refer to the [example tile](https://github.com/pivotal-cf-experimental/ops-manager-example/releases)

# Quality & testing Requirements and guidelines

To release a brand new product to a customer, it may go through several stages of release. Each of these stages has different levels of visibility to customers and associated quality and testing requirements that must be met.

These are detailed in full [here](partners/releases.html)
