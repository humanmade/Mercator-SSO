# Mercator SSO
Single Sign-On component for [Mercator](https://github.com/humanmade/Mercator).

Allows you to share cookies between all sites on the same subdomain.

## Requirements
Mercator requires WordPress 3.9 or newer for the new sunrise processes. Mercator
also requires PHP 5.3+ due to the use of namespaced code.

## Installation
Include the file `sso.php` from your `sunrise.php` in the same way you include Mercator itself.

For example:

```php
<?php
// Default mu-plugins directory if you haven't set it
defined( 'WPMU_PLUGIN_DIR' ) or define( 'WPMU_PLUGIN_DIR', WP_CONTENT_DIR . '/mu-plugins' );

require WPMU_PLUGIN_DIR . '/mercator/mercator.php';
require WPMU_PLUGIN_DIR . '/mercator-sso/sso.php';
```

Optionally you can use `sso-multinetwork.php` as well if you're running
a multinetwork site.

## Filters
You can modify SSO behaviour for example in a local environment with the
following filters in `sunrise.php`:

**mercator.sso.enabled**

```php
// Disable SSO
add_filter( 'mercator.sso.enabled', '__return_false' );
```

**mercator.sso.multinetwork.enabled**

```php
// Disable Multinetwork SSO
add_filter( 'mercator.sso.multinetwork.enabled', '__return_false' );
```

## License
Mercator is licensed under the GPLv3 or later.

## Credits
Created by Human Made for high volume and large-scale sites, such as [Happytables](http://happytables.com/). We run Mercator SSO on sites with millions of monthly page views, and thousands of sites.

Written and maintained by [Ryan McCue](https://github.com/rmccue). Thanks to all our [contributors](https://github.com/humanmade/Mercator-SSO/graphs/contributors).

Mercator builds on concepts from [WPMU Domain Mapping][], written by Donncha O'Caoimh, Ron Rennick, and contributors.

Mercator relies on WordPress core, building on core functionality added in [WP27003][]. Thanks to all involved in the overhaul, including Andrew Nacin and Jeremy Felt.

[WPMU Domain Mapping]: http://wordpress.org/plugins/wordpress-mu-domain-mapping/
[WP27003]: https://core.trac.wordpress.org/ticket/27003

Interested in joining in on the fun? [Join us, and become human!](https://hmn.md/is/hiring/)
