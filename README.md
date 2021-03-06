puppet-ghostbuster
==================

[![Build Status](https://img.shields.io/travis/camptocamp/puppet-ghostbuster.svg)](https://travis-ci.org/camptocamp/puppet-ghostbuster)
[![Gem Version](https://img.shields.io/gem/v/puppet-ghostbuster.svg)](https://rubygems.org/gems/puppet-ghostbuster)
[![Gem Downloads](https://img.shields.io/gem/dt/puppet-ghostbuster.svg)](https://rubygems.org/gems/puppet-ghostbuster)
[![Gemnasium](https://img.shields.io/gemnasium/camptocamp/puppet-ghostbuster.svg)](https://gemnasium.com/camptocamp/puppet-ghostbuster)

When you have dead puppet code hanging around ...
*Who you gonna call ?*


This gems helps puppet users to find dead code by displaying unused classes, defined resources, template and files.

This gems only support PuppetDB APi v4 (PuppetDB 3+)

Usage
-----

```shell
$ find . -type f -exec puppet-lint --only-checks ghostbuster_classes,ghostbuster_defines,ghostbuster_files,ghostbuster_templates {} \+
```

Environment variables
---------------------

### PUPPETDB_URL

The url or the PuppetDB. Defaults to `http://puppetdb:8080`

### PUPPETDB_CACERT_FILE

Your site’s CA certificate

### PUPPETDB_CERT_FILE

An SSL certificate signed by your site’s Puppet CA

### PUPPETDB_KEY_FILE

The private key for that certificate

Example output
--------------

TODO
```
$ find . | puppet-lint --only-checks ghostbuster_classes,ghostbuster_defines,ghostbuster_files,ghostbuster_templates
```
