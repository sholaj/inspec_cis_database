# inspec_cis_database

This repo is for fabricating Compliance as Code.

The purpose of this repo is to scan infrastructure and report on compliance issues, security risks, and outdated software. It provides a centrally managed key to continuously and automatically check and enforce security and compliance requirements using InSpec, an open source testing framework for specifying compliance, security, and policy requirements.

The profiles in this repo scan for configuration-drift issues such as password complexity rules, database configuration, whether packages are installed/patched with security patches etc. When drift is detected, it is reported as a centrally distributed and can be automatically remediated using Chef and/or Ansible.

CIS profiles that we want to run against a set inventory, it will imported in the repository for the InSpec execution playbooks.

## Database Platforms

- **MSSQL** (SQL Server 2008, 2012, 2014, 2016, 2017, 2018, 2019, 2022)
- **Oracle** (11g, 12c, 18c, 19c)
- **Sybase ASE** (15, 16)
- **PostgreSQL** (15)

## Support Information

```
GTS Orchestration and Automation
App Code:     CHF
```
