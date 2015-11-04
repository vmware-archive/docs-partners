---
title: Release Cycle
---

Releasing a product to Pivotal Cloud Foundry (PCF) involves four phases, detailed below:

## <a id='alpha'></a>Phase 1: Alpha

Alpha is the initial development phase for a product. The product is under constant churn and refactoring, and may not be feature-complete.

This is an internal testing phase with no exposure to customers, so there are no quality requirements in this phase.

## <a id='closed-beta'></a>Phase 2:  Closed Beta

During **Closed Beta**, releases of the product are exposed to a limited pool of users in order to gather feedback. This feedback is used to drive further development.

A status of Closed Beta informs users that the product may be unstable and should not be used in production.

A product should remain in Closed Beta while:

- Changes may break product function or cause loss of data
- Users may experience major bugs
- Users may have to delete and reinstall tiles rather than upgrading

Developers make products in closed beta available to specific groups or individual customers on [Pivotal Network](http://network.pivotal.io).

### Requirements
Products in Closed Beta must meet the following requirements:

* The product must be tested on at least one IaaS (either AWS, vSphere or Openstack).

* The product tile must target the [stemcell version](https://network.pivotal.io/products/stemcells) of the latest available Pivotal OpsManager.

* The release notes must make the following clear:

  * The product is **not** suitable for use in production, due to potential data loss and lack of support.

  * To move to the next version of the product, users will need to delete the old tile and install a new one, as there will be no upgrade path.


### Test Coverage
The following test scenarios must be validated:

* The product tile can be installed successfully without any errors.
* The product tile can be deleted successfully and leaves no trace behind.
* The product tile has a valid stemcell reference that is available on [Pivotal Network](https://network.pivotal.io/products/stemcells).
* The desired feature set of the product has being validated as functional enough to provide the desired feedback.

### Steps to Release
1. Log into [Pivotal Network](http://network.pivotal.io) and create a new release for your product by completing the following steps.
  1. Populate all of the required fields.
  1. Make sure the release version states **BETA**.
  1. Make sure the release description states this product is not upgradeable and may suffer data loss.
1. E-mail your Pivotal contact asking for them to validate the product and release and make it viewable to customers. Please provide some basic instructions on how to validate the new feature set.

## <a id='public-beta'></a>Phase 3: Public Beta

In Public Beta, your product is available to the general public. This allows you to gather more feedback, from a wider pool of users. It also increases public awareness of the product, facilitating marketing and advertising. As development continues, a series of product versions may appear in Public Beta.

**Public Beta** is appropriate for your product if it meets the following conditions:

- You are confident that further development will not entail breaking changes or data loss.
- The tile is upgradeable.
- You need user feedback to discover minor bugs and evaluate existing features.
- The product does not contain the full set of features intended for the final release.

Products in Public Beta are available on [Pivotal Network](http://network.pivotal.io) to any user with a free Pivotal Network account.

### Requirements
Products in Public Beta must meet the following requirements: 

* The product meets all requirements for [**Closed Beta**](#closed-beta).

* The tile is upgradeable between versions. It does not require the customer to un-install the previous version. The product must support upgrade paths from any minor version, including its patches, to the next minor verion and its patches.

* Your product tile has being validated at least once on all available IaaS (vSphere, AWS, Openstack).

* There is no data or configuration loss between upgrades of tile versions.

* You can respond to discovery of a security flaw on the [Common Vulnerabilities and Exposures (CVE) list](https://cve.mitre.org/cve/index.html) on a reasonable timeline. This includes vulnerabilities in your stemcell or within one of the components of your tile. For reference, Pivotal aims to respond to all critical CVEs within 48 hours.

* As a vendor you feel comfortable you can now support this tile for customers

### Test Coverage
The following test scenarios must be validated:

* Testing requirements for **Closed Beta** have been met.
* Upgrades work correctly.
* There is no data or configuration loss between versions.
* The service is available and working after an upgrade.
* Your product integrates properly with Pivotal Cloud Foundry, including:
  * Registered routes
  * UAA
  * Service brokers

### Steps to Release

1. Log into [Pivotal Network](http://network.pivotal.io) and create a new release for your product.
  1. Populate all of the required fields
  1. Make sure the release version states **BETA**.
1. E-mail your Pivotal contact asking for them to validate the product and release it to customers. Please provide some basic instructions on how to validate the new feature set. We will validate the upgrade scenario and data persistence.

## <a id='ga'></a>Phase 4: Generally Available

A product becomes **Generally Available** when:

- It is ready for production.

- You are ready to charge money for this product and provide support guarantees to your customers.

- Your product's full set of features meet the standards of quality that your company wishes to uphold.

### Requirements
**Generally Available** products must meet the following requirements: 

* All requirements for [**Public Beta**](#public-beta) are met.
* It is considered production ready.
* You can provide customer support.
* "Go to market work" is complete.
* The product can scale vertically.
* If appropriate, the product can scale horizontally to meet the standards of 'high availability'.
* If appropriate, the product supports zero downtime deployment.
* Product installation does not require an internet connection.

### Test Coverage
The following test scenarios must be validated:

* All testing scenarios for **Public Beta**.
* Vertical scaling, such as increasing the amount of RAM and/or CPU, improves performance and does not result in data loss.
* Horizontal Scaling:
  * Scaled out nodes function correctly.
  * Removing a node does not result in downtime.
* Adequate unit and functional tests to ensure high quality.

<!-- * Zero-downtime deployments:
  * If the product has HA components" -->

### Steps to Release
1. Log into [Pivotal Network](http://network.pivotal.io) and create a new release for your product. Populate all of the required fields.
1. E-mail your Pivotal contact asking for them to validate the product and release and make it discoverable to customers. Please provide some basic instructions on how to validate the new feature set. We will validate the upgrade scenario and data persistence.
