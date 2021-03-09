# Overview

> ARIA is a collaboration between JPL and Caltech to exploit radar and optical remote sensing, GPS, and seismic observations for hazard science and response.

## Background

For more information on the science and technology behind the ARIA project, please visit the [ARIA Homepage](https://aria.jpl.nasa.gov)

For design documentation related to the ARIA project's software, please consult the [Wiki](https://aria.atlassian.net/wiki/spaces/ARIA/overview).

# Usage

## Getting Started

The ARIA suite of software is implemented and deployed as a set of _pipelines_ that are independently managed and run for various science use cases.

The best way to get started with ARIA software is to choose a science pipeline use case, and review / use / deploy the code for that use case. The remainder
of this document organizes software information based on pipelines.

## Pipelines

### Coseismic Pipeline

_The Coseismic pipeline automatically identifies earthquake events globally, and generates interferograms for before and after the earthqake event_

[DATA FLOW DIAGRAM HERE]

The following GitHub repositories together represent the coseismic pipeline:
- https://github.com/aria-jpl/coseismic_product
- https://github.com/aria-jpl/ariamh
- https://github.com/al-niessner/coseismic_enumerator

Please consult the respective `README.md` files for each of the above repositories for installation directions per component.

# Developer Guides

In this section, we outline the development process for ARIA software, and offer guidance on contributing code, new issues, or documentation.

## GitHub

We leverage Public GitHub for our code development, and our organization is available at: https://www.github.com/aria-jpl

### Repositories

When creating a new repository (or updating an existing one to be compliant), first consider the following principles:
- Consistency in how documentation for a repo is made available
- Consistency in how users / contributors file tickets
- Clarity in how to build and run repo software
- Consistency in naming of artifacts associated with a repository

For ARIA software, we strive to utilize an industry-standards based approach to designing repositories.

The following is a list of curated guidelines for creating (or updating) a repository to follow the above principles:

**Use a Standard Repo Name**

Most repositories will be related to a given ARIA _pipeline_ (see #pipeline section above). The naming convention suggested for pipeline
related repositories is the following: `[pipeline]_[component]`. For example, the _Enumerator_ component of the _Coseismic pipeline_ should
have a repo name of `coseismic_enumerator`.

### Issues

**Ensure Issue Templates are Activated**

Issue templates help ensure consistent and readable tickets for all team members. Follow the [directions from GitHub](https://docs.github.com/en/free-pro-team@latest/github/building-a-strong-community/configuring-issue-templates-for-your-repository) to activate your repository's issue templates. Namely, Bug Reports and Feature Requests should have templates
available for developers to utilize. The standard GitHub templates for Bug Reports and Feature Requests are acceptable to use.

In addition to Bug Reports and Feature Requests, optionally create a template for Task Issues. This type of ticket represents general tasks
that are requested to be performed, separate from new features or bugs. Please use the below template text for this type of ticket:

```
<!--- Provide a general summary of the issue in the Title above -->
<!--- NOTE: in the right hand bar, please also specify: -->
<!---       * assignee: the person tasked with resolving the issue -->
<!---       * labels: the type of issue

**Brief Description**
<!--- Provide a brief description, in plain english, of the task you are proposing -->

**Expected Behavior**
<!--- Tell us what should happen -->

**Current Behavior**
<!--- Tell us what happens instead of the expected behavior -->
<!--- NOTE: if this issue is a bug, include an unambiguous set of steps to reproduce the issue -->

**Suggested Ideas on Resolution**
<!--- Optionally provide an idea for how to resolve the issue, implementation-wise -->
```

An example for the type of capability that should be present after completing the template issue setup process for your repository is the menu
available here: https://github.com/aria-jpl/coseismic_product/issues/new/choose


### README

**Create Useful README Documentation**

A good `README.md` is an essential for others to utilize and contribute towards a repository. For the purposes of ARIA, please use
the following `README.md` template for your repository and fill out all relevant fields:

~~~
# <REPO NAME>
> Single sentence describing the purpose of your repo

More detailed description of your repository

![](header.png) [Screenshot of your software, if applicable]

## Build Instructions

[Modify as/if needed]

e.g.

Built using the ARIA HySDS Jenkins Continuous Integration (CI) pipeline.

More information about this process can be found [here](https://hysds-core.atlassian.net/wiki/spaces/HYS/pages/455114757/Deploy+PGE+s+onto+Cluster)

## Run Instructions

[Modify as/if needed and add any customizations for your code]

e.g.

You may run your customized PGE via two methods that are documented below:
- An [on-demand (one-time) job](https://hysds-core.atlassian.net/wiki/spaces/HYS/pages/378601499/Submit+an+On-Demand+Job+in+Facet+Search)
- [Create a trigger rule](https://hysds-core.atlassian.net/wiki/spaces/HYS/pages/442728660/Create+Edit+Delete+Trigger+Rules) to invoke your PGE based on conditions

## Release History

* 0.2.1
    * CHANGE: Update docs (module code remains unchanged)
* 0.2.0
    * CHANGE: Remove `setDefaultXYZ()`
    * ADD: Add `init()`
* 0.1.1
    * FIX: Crash when calling `baz()` (Thanks @GenerousContributorName!)
* 0.1.0
    * The first proper release
    * CHANGE: Rename `foo()` to `bar()`
* 0.0.1
    * Work in progress


## Contributing

1. Create an GitHub issue ticket describing what changes you need (e.g. issue-1)
2. Fork this repo (<https://github.com/aria-jpl/repo/fork>)
3. Make your modifications in your own fork
4. Make a pull-request in this repo with the code in your fork and tag the repo owner / largest contributor as a reviewer

## Support

Any specific contact information regarding leadership / maintenance of this repository

~~~

### Branches

Ensure that your repository has branches with the following names:
- `master` - branch that contains the repo public and latest stable release code
- `develop` - branch that contains the repo's latest development code
- `issue-XYZ` - branches that relate to specific GitHub ticket issues

### Pull Requests

For all pull requests:
- An associated GitHub ticket should be available to reference
- A default reviewer(s) should be assigned for newly created tickets, please see [GitHub documentation](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/enabling-required-reviews-for-pull-requests) for enabling this feature automatically.

# Support
