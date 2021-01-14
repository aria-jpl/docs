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

Follow the directions from GitHub to activate your repository's issue templates. Namely, Bug Reports and Feature Requests should have templates
available for developers to utilize. The standard GitHub templates for Bug Reports and Feature Requests are acceptable to use.

In addition to Bug Reports and Feature Requests, we'd like to also create a template for Task Issue. This type of ticket represents general tasks
that are requested to be performed, separate from new features or bugs. Please use the below template text for this type of ticket:

```
<!--- Provide a general summary of the issue in the Title above -->
<!--- NOTE: in the right hand bar, please also specify: -->
<!---       * assignee: the person tasked with resolving the issue -->
<!---       * labels: the type of issue
<!---       * milestone: the milestone number this issue should be resolved by -->

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


### Documentation

**Create a Useful README**

A good `README.md` is an essential for others to utilize and contribute towards a repository. For the purposes of ARIA, please use
the following `README.md` template for your repository and fill out all relevant fields:

~~~
# <REPO NAME>
> Single sentence describing the purpose of your repo

More detailed description of your repository

![](header.png) [Screenshot of your software, if applicable]

## Installation

OS X & Linux:

```sh
TBD
```

Other deployment environment(s):

```sh
TBD
```

## Usage example

A few motivating and useful examples of how your product can be used. Spice this up with code blocks and potentially more screenshots.

_For more examples and usage, please refer to the [Wiki][wiki]._

## Development setup

Describe how to install all development dependencies and how to run an automated test-suite of some kind. Potentially do this for multiple platforms.

```sh
make install
npm test
```

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

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

<!-- Markdown link & img dfn's -->

## Support

Any specific contact information regarding leadership / maintenance of this repository

~~~

# Support
