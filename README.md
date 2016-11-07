![geniem-github-banner](https://cloud.githubusercontent.com/assets/5691777/14319886/9ae46166-fc1b-11e5-9630-d60aa3dc4f9e.png)
# WordPress Security Plugin Collection
[![Latest Stable Version](https://poser.pugx.org/devgeniem/wp-sanitize-accented-uploads/v/stable)](https://packagist.org/packages/devgeniem/wp-security-collection) [![Total Downloads](https://poser.pugx.org/devgeniem/wp-security-collection/downloads)](https://packagist.org/packages/devgeniem/wp-security-collection) [![Latest Unstable Version](https://poser.pugx.org/devgeniem/wp-security-collection/v/unstable)](https://packagist.org/packages/devgeniem/wp-security-collection) [![License](https://poser.pugx.org/devgeniem/wp-security-collection/license)](https://packagist.org/packages/devgeniem/wp-security-collection)

This is WordPress plugin collection which adds security enhancements like audit logs and password hardening.

## Reasons
This package was created to handle multiple projects with `composer update`. We just include this collection into our `composer.json` and stick to the guidelines about which plugins should be included here. WordPress evolves with time and some plugins will propably be pointless at some point, if that happens we will remove those unneccessary plugins.

## Installation
```
$ composer require devgeniem/wp-security-collection
```

## Guidelines
We only want to add minimal plugins which enhance small part of WordPress.

### Password hardening
WordPress should require long passwords and store them with secure hashes.

### Audit logs
WordPress should produce audit logs which we can use to analyse user actions.

## Requirements
* >= PHP 7.0
* WordPress
* Use composer to update your site rather than using WordPress auto updates

### Composer.json settings
For correct installation your project should define following installation paths in `extra` section:
```
extra: {
    "installer-paths": {
      "web/app/mu-plugins/{$name}/": ["type:wordpress-muplugin"],
      "web/app/plugins/{$name}/": ["type:wordpress-plugin"]
    },
    "dropin-paths": {
      "web/app/": ["type:wordpress-dropin"]
    }
}
```

We use bedrock styled names for `wp-content`. Replace `web/app` according for your project.

## Maintainers
[Onni Hakala](https://github.com/onnimonni)

## Changelog
[See the included CHANGELOG.md](CHANGELOG.md)

## License
Respect the licenses of used libraries. This readme and composer are licensed under MIT
