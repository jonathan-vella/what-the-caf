# Modernize

Implement and test the required application and database changes to ensure the migrated application works as expected in the cloud.

## Application Modernization

### Application: Implement Required Changes

#### Compatibility Tasks

1. REFACTOR: Nuget packages for all references
1. REFACTOR, REARCHITECT: Split non-packagable references into seperate de-coupled services (Crystal
   Reports, ABCPDF...)
1. REHOST / REFACTOR: Remove GO statements from SQL or use SQL MI
1. REFACTOR, REARCHITECT: Split sprocs, views and queries that rely on cross-db joins into multiple
   Db calls at the Data Layer. Or use SQL MI.
1. REHOST: Turn on simple-auth with AAD for authentication
1. REHOST: Replace SMTP service with SendGrid. Refactor send mail calls if not configurable with AppSettings.
1. REHOST / REFACTOR: Refactor DateTime helper to support UTC time, Refactor sprocs to take a `@now`
   parameter. Or, use SQL MI.
1. Use SQL or Redis Session State provider

### Deploy to Test Env

👷🏻‍♀️🚧👷🏻‍♂️ (WIP)

### Hybrid Connection for DB Access
### Smoke Tests + Minimum UAT Tests

## Database migration
### Implement Required Changes
### Application: Implement Required Changes
### Deploy to Cloud Test Environment
### Migrate data sample

## General
### User Acceptance Tests