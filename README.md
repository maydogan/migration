# Migration Module for Drupal #

## Introduction ##

This repository contains a Drush module and migrate_d2d module for migration from D6 to D7.

__Drush Module__ : This module is used for converting some several fields to another separate fields in a content type. This separation operation makes field-to-field migration easy. Additionally, this module can dump node variables anytime and fix translation matches after migration process.

__Migrate Module__ : This module is the main migration module.

This module is capable of doing

* Content type
* Taxonomy
* File
* User
* Menu

migrations while processing dependencies between these elements.

Content types with related fields and taxonomy vocabularies should be created before running these migrations but there is no need to create vocabulary terms inside a taxonomy because, migration automatically transfers the terms.


## Requirements ##

### For Drupal 6 ###

* [Date](https://drupal.org/project/date)
* [Calendar](https://drupal.org/project/calendar) (optional)

### For Drupal 7 ###

* [Migrate](https://drupal.org/project/migrate) (tested for version 2.5)
* [Drupal-to-Drupal Data Migration](https://drupal.org/project/migrate_d2d) (tested for version 2.0)
* [Date](https://drupal.org/project/date)


## Notes ##

### Module Changes ###

* SWFUpload -> [jQuery File Upload](https://drupal.org/project/jquery_file_upload)

### Problems & Solutions ###

* When Date Popup is used, related field does not updated with correct data from the database. Probably, this is a problem of local testing environment.
* After deleting some content types, SQL query changes and Drush module should be updated to fit these changes.

## Usage ##

* Wonder what is all about? See [INFO](doc/INFO.md) file.
* Want to know how to use this package? See [USAGE](doc/USAGE.md) file.

## License ##

This package is licensed under [APACHE License v2.0](http://www.apache.org/licenses/LICENSE-2.0.html)
