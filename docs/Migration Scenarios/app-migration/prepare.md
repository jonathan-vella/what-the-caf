# Prepare

Find unique details and needs for the application being migrated, define re-architecture needs and required code and database changes to ensure the application will work as expected once migrated.

## Architect Design Review

We recommend that an Architecture review is conducted at the beginning of each App migration (during **Prepare** phase) and again just before **Production Deploy**. Engage a FastTrack for Azure Engineer to perform the review. The engineer will follow the review process described in [FastTrack for Azure Architectural / Solution Review and Guidance Framework].

> 📖 See also **[Microsoft Azure Well-Architected Framework]**

> 💡 You can perform a well-architected assessment at any time by using the **[Well-Architected Review tool]**.


## App Service Migration Assessment

Use the **[App Service Migration Assistant]** or a third party tool to scan and generate a report on the current state of the Web App. 

## Data Migration Assessment

Use the **[Database Migration Assistant]** to evaluate the Databases for migration.

## Other prepare steps

* Define Migration Strategy
* Identify Required Changes
* CI/CD Considerations
* Setup Cloud Test Environment

<!-- LINKS -->

[FastTrack for Azure Architectural / Solution Review and Guidance Framework]:https://github.com/Azure/fta-architecturalreview/blob/master/articles/introduction.md
[Microsoft Azure Well-Architected Framework]:https://docs.microsoft.com/en-us/azure/architecture/framework/
[Well-Architected Review tool]:https://docs.microsoft.com/en-us/assessments/?mode=pre-assessment&id=azure-architecture-review
[App Service Migration Assistant]:https://appmigration.microsoft.com/
[Database Migration Assistant]:https://datamigration.microsoft.com/scenario/sql-to-azuresqldbmi?step=1
