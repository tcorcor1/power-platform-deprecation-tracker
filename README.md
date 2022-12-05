# Power Platform Deprecation Tracker

Repository designed for tracking and notifiying subscribers on changes to Microsoft Power Platform deprecation pages.

**Tracked pages as of 12/2/2022**:

- [Important changes (deprecations) coming in Power Apps and Power Automate](https://learn.microsoft.com/en-us/power-platform/important-changes-coming)

I would love to track more pages and expand on this idea. If you have suggestions for pages please leave a comment on my [blog post](https://tldr-dynamics.com/blog/power-platform-deprecation-tracker) or drop an issue here.

### How it works

Every 12 hours, an Azure function will scrape pages and check for changes. If it finds updates, it will create a commit and release. If you watch this repo, you will receive an email upon each release.

If you don't want any emails, just star the repo and pop in once in a while to check out the history on the files, i.e. [/pages/powerplatform-deprecations.txt](https://github.com/tcorcor1/power-platform-deprecation-tracker/commits/main/pages/powerplatform-deprecations.txt).

### Tech used

- [HtmlAgilityPack](https://html-agility-pack.net/) - HTML parser written in C# to read/write DOM and supports plain XPATH or XSLT
- [Octokit](https://octokitnet.readthedocs.io/en/latest/) for .NET - A GitHub API client library for .NET
- Azure Functions
