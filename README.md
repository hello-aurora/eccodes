# heroku-buildpack-eccodes

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) working with [`heroku-20`](https://devcenter.heroku.com/articles/stack) for vendoring the [ecCodes](https://confluence.ecmwf.int/display/ECC/) library into your project.

## Install

In your project root:

`heroku buildpacks:add https://github.com/hello-aurora/eccodes --index 1 --app HEROKU_APP_NAME`

## Usage

This buildpack install ecCodes and you will get the following commands available:

- `codes_count`
- `codes_info`
- `codes_split_file`
- `bufr_compare`
- `bufr_copy`
- `bufr_count`
- `bufr_dump`
- `bufr_filter`
- `bufr_get`
- `bufr_ls`
- `bufr_set`
- `grib_compare`
- `grib_copy`
- `grib_count`
- `grib_dump`
- `grib_filter`
- `grib_get`
- `grib_get_data`
- `grib_index_build`
- `grib_ls`
- `grib_set`
- `grib_to_netcd`

To see more about the usage, please refers to their [documentation](https://confluence.ecmwf.int/display/ECC/Documentation).

## Clear cache

Since the installation is cached you might want to clean it out due to config changes.

1. `heroku plugins:install heroku-repo`
2. `heroku repo:purge_cache --app HEROKU_APP_NAME`
