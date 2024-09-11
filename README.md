# Express Release Strategy

## Major Version Releases

* Major versions are released when breaking changes are required.
* A new major version will not be released sooner than one year after the last major version release.

## Version Lifecycle

* **CURRENT:** A new major version is designated as CURRENT upon release. It is available but not the `latest` version on npm for six months.
* **ACTIVE:** After six months, the CURRENT version becomes ACTIVE and is the `latest` version on npm for a minimum of 12 months.
<!-- * During this 12-month ACTIVE period, a new major version can be released, but it cannot be released sooner than six months into the ACTIVE period of the current version. -->
* **MAINTENANCE:** When a new major version becomes ACTIVE, the previous major version enters MAINTENANCE. The MAINTENANCE period lasts for 18 months.

## Generate the SVG

```sh
npx lts --start 2024-01-01 --end 2027-01-01 -d "$PWD/schedule.json" -g "$PWD/schedule.svg" -m -n Express

npx svgo "$PWD/schedule.svg"
```

![express release schedule](schedule.svg)
