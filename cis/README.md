# Role: cis

This role stores InSpec controls for MSSQL, Oracle, Sybase, and PostgreSQL databases that perform CIS checks against known issues. The profiles will be imported in a different repository called `linux-inspec` (execution repo) which will execute the InSpec controls against a set inventory.

This role performs the following functions:

- Allows Ansible Tower/AAP2 to import the profiles stored here and execute the InSpec controls against a set inventory

## Version & Author

```
VER  | [MM/DD/YYYY]  | COMMENTS                                              [AUTHOR]
1.0  | [04/15/2026]  | Initial Version                                       [InSpec Compliance Team]
                      | Create CIS profiles for MSSQL 2008-2022
                      | Create CIS profiles for Oracle 11/12/18/19
                      | Create CIS profiles for Sybase 15/16
                      | Create CIS profiles for PostgreSQL 15
```

## Requirements

```
This role is imported through the requirements.yml file in the execution repository
corresponding with the project CHF_DEVTEST_Proj_CfgMan_InSpec_Scan in Ansible Tower.
```

## Example Usage

```
After the role is imported in Ansible Tower the profiles can be executed via the
job template CHF_DEVTEST_NA_Job_CfgMan_Database.
```

## Variables defaults

```
None
```

## Variable files

```
None in this repository, the variable files are stored in the execution repository.
```

## InSpec Testing

```
inspec check cis/files/profiles/ssc-cis-mssql2022-1.1.0-1/
inspec check cis/files/profiles/ssc-cis-oracle19-1.2.0-1/
inspec check cis/files/profiles/ssc-cis-sybase16-1.0.0-1/
inspec check cis/files/profiles/ssc-cis-postgres15-1.0.0-1/
```

## Profiles

Folder naming: `ssc-cis-<plat><ver>-<cis_version>-1`, where `<cis_version>`
matches the `version:` field in each profile's `inspec.yml`.

| Profile | Platform | CIS Benchmark | Controls |
|---------|----------|---------------|----------|
| ssc-cis-mssql2012-1.6.0-1 | MSSQL 2012 | CIS Microsoft SQL Server 2012 v1.6.0 | 46 |
| ssc-cis-mssql2014-1.5.0-1 | MSSQL 2014 | CIS Microsoft SQL Server 2014 v1.5.0 | 46 |
| ssc-cis-mssql2016-1.4.0-1 | MSSQL 2016 | CIS Microsoft SQL Server 2016 v1.4.0 | 46 |
| ssc-cis-mssql2017-1.3.0-1 | MSSQL 2017 | CIS Microsoft SQL Server 2017 v1.3.0 | 68 |
| ssc-cis-mssql2019-1.5.0-1 | MSSQL 2019 | CIS Microsoft SQL Server 2019 v1.5.0 | 69 |
| ssc-cis-mssql2022-1.1.0-1 | MSSQL 2022 | CIS Microsoft SQL Server 2022 v1.1.0 | 72 |
| ssc-cis-oracle12-3.0.0-1 | Oracle 12c | CIS Oracle Database 12c v3.0.0 | 91 |
| ssc-cis-oracle18-1.0.0-1 | Oracle 18c | CIS Oracle Database 18c v1.0.0 | 91 |
| ssc-cis-oracle19-1.2.0-1 | Oracle 19c | CIS Oracle Database 19c v1.2.0 | 91 |
| ssc-cis-oracle21-1.2.0-1 | Oracle 21c | CIS Oracle Database 21c v1.2.0 | 91 |
| ssc-cis-oracle23-1.1.0-1 | Oracle 23c | CIS Oracle Database 23c v1.1.0 | 91 |
| ssc-cis-sybase15-1.0.0-1 | Sybase ASE 15 | CIS SAP ASE 15 v1.0.0 | 7 |
| ssc-cis-sybase16-1.0.0-1 | Sybase ASE 16 | CIS SAP ASE 16 v1.0.0 | 84 |
| ssc-cis-postgres15-1.0.0-1 | PostgreSQL 15 | CIS PostgreSQL 15 v1.0.0 | 59 |

## Support Information

```
GTS Orchestration and Automation
App Code:     CHF
```
