# Geokettle ('geokettle')

**Part of the BAS Ansible Role Collection (BARC)**

Installs the Geokettle (http://www.spatialytics.org/projects/geokettle/) data processing suite.

## Overview

* Downloads Geokettle installation file
* Installs using the geokettle default configuration

## Usage

### Requirements

There no core
### Variables

Variables used in default virtual host `/etc/apache2/sites-available/default`:

* `geokettle_version`
    * Sets the Geokettle version this role should install
    * Currently this variable is only used to download the relevant GeoServer version, in future this may be used to configure different versions as may be needed.
    * This variable **MUST** be a valid Geokettle version, as determined by [Geokettle](http://www.spatialytics.org/projects/geokettle/).
    * This variable **SHOULD** be set to the current stable GeoServer version.
    * Default: "2.5"
* `geokettle_download_url`
    * Default: "http://netcologne.dl.sourceforge.net/project/geokettle/geokettle-2.x/2.5/geokettle_2.5.deb"
* `geokettle_deb_staging_path`
    * Default: "/tmp/"

## Contributing

This project welcomes contributions, see `CONTRIBUTING` for our general policy.

### Committing changes

The [Git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow/) workflow is used to manage development of this package.

Discrete changes should be made within *feature* branches, created from and merged back into *develop* (where small one-line changes may be made directly).

When ready to release a set of features/changes create a *release* branch from *develop*, update documentation as required and merge into *master* with a tagged, [semantic version](http://semver.org/) (e.g. `v1.2.3`).

After releases the *master* branch should be merged with *develop* to restart the process. High impact bugs can be addressed in *hotfix* branches, created from and merged into *master* directly (and then into *develop*).

### Issue tracking

Issues, bugs, improvements, questions, suggestions and other tasks related to this package are managed through the BAS Web & Applications Team Jira project ([BASWEB](https://jira.ceh.ac.uk/browse/BASWEB)).

## License

Copyright 2015 NERC BAS. Licensed under the MIT license, see `LICENSE` for details.
