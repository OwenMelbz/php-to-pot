# PHP to .POT Generator

This is a really simple command line tool which generates a .pot or .po file based off language strings that it finds within the defined directory.

Currently it simply accepts 2 paths, an input - which should be a directory of templates, and an output, which is typically a .pot file.

## Installation
1. `composer install owenmelbz/php-to-pot`

## Optional
Create a composer script to save your little fingers e.g

```
"scripts": {
	"makepot": "./vendor/bin/php-to-pot -i ./my-template-directory -o ./translation-template.pot"
}
```

You can then just run `composer run makepot` to generate your file when needed.

## Usage
The tool has only 2 params

1. -i/--in (a directory containing files you want to generate translations from)
2. -o/--out (the path/filename of the generated .pot)

e.g

```
./vendor/bin/php-to-pot -i ./my-templates -o translation-template.pot
```

## Support
- Magento 2
- Wordpress
- Laravel Blade
- Anything else that uses .php extension and a list of the following translation functions

__
n__
p__
_e
d__
dn__
dp__
np__
dnp__
noop__
gettext
ngettext
pgettext
dgettext
dngettext
dpgettext
npgettext
dnpgettext
noop

## Disclaimer

Under the hood, this just interfaces with https://github.com/oscarotero/Gettext to allow developers to generate .pot files to send to translators to create the actual .po and .mo files.
