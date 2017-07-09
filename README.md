# fusiondirectory-schemas

This role downloads FusionDirectory with the plugins and places the schema files on a server.

As the files are downloaded on the control machine, the target doesn't need an internet connection.

## Requirements

None

## Role Variables

| Name                            | Default/Required   | Description                                                                                     |
|---------------------------------|:------------------:|-------------------------------------------------------------------------------------------------|
| `global_cache_dir`              | :heavy_check_mark: | Path to a directory on the control machine where FusionDirectory is downloaded and extracted to |
| `fusiondirectory_major_version` | `1.0`              | Major version of FusionDirectory, this is required in the download URL                          |
| `fusiondirectory_version`       | `1.2`              | FusionDirectory version to download and extract                                                 |
| `slapd_schema_dir`              | `/etc/ldap/schema` | Path where the downloaded schemas are placed in a subdirectory called `fusiondirectory`         |

## Dependencies

None

## Example Playbook

```yml
- hosts: ldap
  roles:
  - fusiondirectory-schemas
    slapd_schema_dir: /etc/openldap/schema
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

## Author Information

- [Janne Heß](https://github.com/dasJ)
