# Application Inventory

Obtain a detailed customer application inventory which allows tracking of relevant information for each app. 

## Create Application Map

Start by documenting:

* Identify Apps and Data Repositories
* Identify Inter-App Dependencies
* Remote dependencies (WCF, SQL, HTTP, SFTP)

## Application Assessment Checklist

Use this checklist to learn the per App needs.

### Web tier

1. What version .NET Framework?
1. Web Forms? | MVC? (What version) | Web API?
1. Which Session State Provider?
1. Do App Pools have user Identity (other than LOCALSYSTEM)?
1. Any ISAPI filters?
1. File system access?
1. Virtual directories?
1. Logging configuration and sinks
1. APM SDK version and details (Application Insights, New Relic)
1. DateTime: use of non-UTC times (DateTime.Now, type = local)
1. Redis cache client code using Lazy pattern?

### WCF services

1. WCF services? 
1. Same VM (tier) as Web or separate?
1. Any non HTTP bindings?
1. HTTPS bindings? 
1. What type auth?

### DB tier

1. Sharded DBs? Shard master?
1. SQL Server using local Timezone or UTC? Using GETDATE()?
1. SSRS? SSAS? SSIS?
1. Any other storage?
1. Lots of large Blobs in SQL DBs? (PDFs, Images)
1. Online DB used for Reports?

### IAM

1. How are users Authenticated?
1. How are users Authorized?
1. ASP.NET Web Forms Auth? ASP.NET Identity Framework? | Identity Server?
1. OAuth / OpenId compliant Auth?
1. Usernames and Passwords stored in Database?
1. How are roles & groups managed inside the app?
1. Check for NTLM or AD

### Networking

1. DNS settings
1. Root CA, SSL certs, etc
1. Can server see Internet on 443, 80, etc
1. Default gateway
1. DNS server and settings
1. SNAT exhaustion risk?

### SMTP

1. Does the App send email?

### Performance

1. Concurrent and total users?
1. Peak requests per minute/second (RPM/RPS)?
1. RPM per (web) core (if known)?
1. DB requests per Page request (if known)?
1. Percent sync vs async entry points
1. CDN used?
1. Output cache used?
1. Caching objects used?
1. Session state, Web Forms Session?
1. Default Session State readonly?

### Compatibility Checks

If the answer to any of these questions is yes, some refactoring and/or rearchitecting may be required to make the solution compatible with Azure App Services.

#### Web

1. Any MSI installed components?
1. Any GAC'ed DLLs?
1. Any COM or COM+ components?
1. Any binary references?
1. Any ports other than 80 and 443 used?

#### DB

1. Any GO statements in SQL?
1. Any cross-DB joins in SQL?
1. Any .NET CLR Functions in SQL?
1. Any SQL MSDTC?
1. Any FILESTREAM?

## Inventory Prioritization

Once inventory has been collated, score each app by complexity and project size, then prioritize into "waves". The first wave should contain a small number of apps as a large amount of "sprint zero" work will be performed that can be reused for subsequent waves.

[Azure Migration Center]:https://azure.microsoft.com/en-us/migration/
[App Service Migration Assistant]:https://appmigration.microsoft.com/
[Migrate your .NET web app or service to Azure App Service]:https://docs.microsoft.com/en-us/dotnet/azure/migration/app-service
[App Service Migration Assistant Migration docs]:https://github.com/Azure/App-Service-Migration-Assistant/tree/master/MigrationDocs
[99.9%]:https://uptime.is/99.9
[Database Migration Assistant]:https://datamigration.microsoft.com/scenario/sql-to-azuresqldbmi?step=1