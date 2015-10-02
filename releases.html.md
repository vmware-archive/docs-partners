---
title: Partner Documentation - Release phases
---

# Release cycle

There are four typical and recommended stages to releasing a product to a customer.

The timelines for moving between each stage will vary by customer and depend upon your product and feature set. Based on experience though, we recommend allowing at least a month for the product to be in Public Beta before moving to GA.

## Phase 0 - Alpha

This is the beginnings of your product, when it is in its development stage. The product may be under constant churn and refactoring and may not be feature complete.

You may be testing this internally, not with customers. So there are no quality requirements at this stage.

## Phase 1 - Closed Beta

Closed Beta is for when you have a version of your product that you feel is relatively stable and you are keen to get feedback on from customers.

It can be made available on [Pivotal Network](http://network.pivotal.io) to specific groups or individual customers upon request.

Being in closed beta gives you the freedom to make breaking changes, fix any big bugs, suffer potential data loss and advise the customer that they need to delete the tile in between versions.

This is useful as you receive customer feedback that may alter your approach to the product and features that you are delivering.

You may release multiple versions of the tile whilst you are in closed beta.

### Requirements
The minimum requirements / characteristics for a product to be in closed beta are:

* Tested on at least one IaaS (either AWS, vSphere or Openstack)
* Not recommended for use in production - due to potential data loss and lack of support
* Targets the [stemcell version](https://network.pivotal.io/products/stemcells) of the latest available Pivotal OpsManager
* Product doesnt have to be upgradeable between versions
  * Expectations set clearly with customers on the release notes they have to delete the tile before installing the next version


### Test coverage
To have confidence that the customer can successfully install the product on their environment and not cause any issues, the following test scenarios should have being validated.

* Tile can be installed successfully without any errors
* Tile can be deleted successfully and leaves no trace behind
* Tile has a valid stemcell reference that is available on [Pivotal Network](https://network.pivotal.io/products/stemcells)
* The desired feature set of the product has being validated as functional enough to provide the desired feedback

### Steps to release
1. Log into [Pivotal Network](http://network.pivotal.io) and create a new release for your product
  1. Populate all of the required fields
  1. Make sure the release version states **BETA**
  1. Make sure the release description states this product is not upgradeable and may suffere data loss.
1. E-mail your Pivotal contact asking for them to validate the product and release and make it viewable to customers
  1. Please provide some basic instructions on how to validate the new feature set

## Phase 2 - Public Beta

Public Beta is for when you have a version of the product that you want to get wider feedback on, announce its public beta availability and you are comfortable requires no more breaking changes as it is more stable.

It will be made available on [Pivotal Network](http://network.pivotal.io) to the general public, only logged in users will be able to download it.

Being in public beta allows you to seek feedback from a wider audience and start advertising and marketing the product. As it is a beta product, there of course may still be a few bugs that encounter and it may not contain the full feature set of the GA product.

This is useful as you can get a wider range of feedback and still continue to iterate on the product and add new features, based on this feedback.

You may release multiple versions of the tile whilst you are in public beta.

### Requirements
The minimum requirements / characteristicsfor a product to be in public beta are:

* Met all requirements of the closed beta phase
* 

### Test coverage

### Steps to release
1. Log into [Pivotal Network](http://network.pivotal.io) and create a new release for your product
  1. Populate all of the required fields
  1. Make sure the release version states **BETA**
  1. Make sure the release description states this product is not upgradeable and may suffere data loss.
1. E-mail your Pivotal contact asking for them to validate the product and release and make it viewable to customers
  1. Please provide some basic instructions on how to validate the new feature set

## Phase 3 - Generally Available
