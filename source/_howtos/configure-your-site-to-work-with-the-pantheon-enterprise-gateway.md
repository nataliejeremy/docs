---
title: How to configure your site to work with the Pantheon Enterprise Gateway
filename: source/_docs/how-to-configure-your-site-to-work-with-the-pantheon-enterprise-gateway.md
---

[Pantheon Enterprise Gateway](https://www.getpantheon.com/pantheon-enterprise-gateway) creates a secure tunnel between your firewall and your public-facing website.

Available for Enterprise customers. [Contact us](https://www.getpantheon.com/contact/enterprise) for more information.

### How do I configure my Pantheon site to use the Pantheon Enterprise Gateway?

After purchasing the Pantheon Enterprise Gateway, a support ticket will be created guiding you through the process. We will need to set up the gateway on our end and you'll need to do a one time setup on your end.

If you’re using the LDAP module you can simply apply the patch [https://www.drupal.org/files/issues/ldap\_php-constant-port\_1.patch](https://www.drupal.org/files/issues/ldap_php-constant-port_1.patch) prepared by one of our Engineers listed on [https://www.drupal.org/node/2283273](https://www.drupal.org/node/2283273) which allows the use of a PHP constant for the port number. If you’re not using the LDAP module, you’ll need to modify your code to accept a PHP constant for the port number. The code in the patch gives a good example of how to do so.

### Once Pantheon Enterprise Gateway is setup, how do I test it with my site?

See [https://github.com/pantheon-<wbr></wbr>systems/soip-example](https://github.com/pantheon-systems/soip-example)

### Is Pantheon Enterprise Gateway a replacement for authentication?

No, Pantheon Enterprise Gateway is not a replacement for authentication, but rather is a [defense-in-depth](http://en.wikipedia.org/wiki/Defense_in_depth_%28computing%29) measure.
