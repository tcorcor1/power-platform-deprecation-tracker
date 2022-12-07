<div align="center">
  <img alt="PowerApps" src="/docs/img/PowerApps_scalable.svg" height="50">
  <img alt="Dataverse" src="/docs/img/Dataverse_scalable.svg" height="50">
  <img alt="PowerAutomate" src="/docs/img/PowerAutomate_scalable.svg" height="50">
  <img alt="PowerBI" src="/docs/img/PowerBI_scalable.svg" height="50">
  <img alt="PowerPages" src="/docs/img/PowerPages_scalable.svg" height="50">
  <img alt="PowerVirtualAgents" src="/docs/img/PowerVirtualAgents_scalable.svg" height="50">
  <h1>Power Platform Deprecation Tracker</h1>
</div>

Repository designed for tracking and notifiying subscribers on changes to Microsoft Power Platform deprecation pages.

**Tracked pages as of 12/6/2022**:

- [Important changes (deprecations) coming in Power Apps and Power Automate](https://learn.microsoft.com/en-us/power-platform/important-changes-coming)
- [Important changes (deprecations) coming in Dynamics 365 Sales](https://learn.microsoft.com/en-us/dynamics365/sales/deprecations-sales)
- [Important changes (deprecations) coming in Dynamics 365 Customer Service](https://learn.microsoft.com/en-us/dynamics365/customer-service/deprecations-customer-service)
- [Important changes (deprecations) coming in Dynamics 365 for Field Service](https://learn.microsoft.com/en-us/dynamics365/field-service/deprecations-field-service)
- [Important changes (deprecations) coming in canvas apps](https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/important-changes-deprecations)
- [Important changes (deprecations) coming in Power Apps portals](https://learn.microsoft.com/en-us/power-apps/maker/portals/important-changes-deprecations)

I would love to track more pages and expand on this idea. If you have suggestions for pages please leave a comment on my [blog post](https://tldr-dynamics.com/blog/power-platform-deprecation-tracker) or drop an issue here.

### How it works

Every 12 hours, an Azure function will scrape pages and check for changes. If it finds updates, it will create a commit and release. If you watch this repo, you will receive an email upon each release.

If you don't want any emails, just star the repo and pop in once in a while to check out the history on the files, i.e. [/pages/powerplatform-deprecations.txt](https://github.com/tcorcor1/power-platform-deprecation-tracker/commits/main/pages/powerplatform-deprecations.txt).

### Tech used

- [HtmlAgilityPack](https://html-agility-pack.net/) - HTML parser written in C# to read/write DOM and supports plain XPATH or XSLT
- [Octokit](https://octokitnet.readthedocs.io/en/latest/) for .NET - A GitHub API client library for .NET
- Azure Functions
