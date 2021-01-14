# ARIA

> ARIA is a collaboration between JPL and Caltech to exploit radar and optical remote sensing, GPS, and seismic observations for hazard science and response.

## Background

For more information on the science and technology behind the ARIA project, please visit the [ARIA Homepage](https://aria.jpl.nasa.gov)

For design documentation related to the ARIA project's software, please consult the [Wiki](https://aria.atlassian.net/wiki/spaces/ARIA/overview).

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
