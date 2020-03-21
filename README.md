# Worksheet for Covid-19 Rapid Response Mapping Project

[![license](https://img.shields.io/github/license/:COVID-19-Rapid-Response-Mapping-Project/:docs.svg)](LICENSE)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

An effort to leverage Kumu.io's data visualization tool with full-stack dev efforts to develop a comprehensive, user-friendly guide to increase United States nationwide access to relief during the Covid-19 pandemic. 

## Table of Contents

- [Goals](#goals)
- [Methodologies](#methodologies)
- [Flows](#flows)
- [Contributing](#contributing)
- [License](#license)

## Goals

Assist those in need of relief or help during the Covid-19 pandemic to easily locate and utilize services available to them.

### Example

[This map](https://embed.kumu.io/db2885359c65081b1b04820706b34e29#regional-covid-19-rapid-response-funds) was produced by Community Credit Labs and is the inspiration for this project. 

### Philosophy / Separation of Concerns

This project focuses on making resources available to those affected by the pandemic.  It is not a statistics dashboard, infection tracker, or the like.  Those things are great, but not relevant to the mission of this project and potentially anxiety / fear-inducing to a target audience looking for help.  Current data objects may be made available to data science projects who may extract useful data or trends (a basic example might be analyzing the types and numbers of nodes across several objects to determine comparatively underserved regions and the type of services lacking).

## Methodologies

### Technical Steps

("need" means MVP, "should" means stretch goal)

 - Kumu takes a JSON object or .xls spreadsheet and generates a visualized map of the data.  We need to generate an appropriate object.
 - We need a front-end to allow users to input resources.
 - We should have someone to vet/dedupe info.
 - We need to automate user-entered form data being converted to one of the above formats.
 - We need a front-end to allow users to find the relevant map.
 - We should provide this data via a publicly-accessible Web API for others to use.
 - There is no API to automatically upload new objects to Kumu.  A script should be written to log in and update the data at a specified time each day.  Perhaps a creative test integrated into the git CI that runs every time a new object is pushed that tests it's ability to login to Kumu and upload the new object.
 - We need ACTION resources as well but not necessarily mapped with Kumu.  These would be things like [Folding@Home](https://foldingathome.org/2020/03/15/coronavirus-what-were-doing-and-how-you-can-help-in-simple-terms/) and call for volunteers to submit resources for unmapped areas.

```
```

### Data Acquisition Steps

  - We need a list of organizations providing relief.
  - We need a selection of relief categories (grant, loan, groceries, medicine, etc.) for organizations to provide.
  - We need a Geographic remit for each organization.
  - We need a short description of the service.
  - We need a link to apply for relief.
  - We need a link to donate, if applicable.
  - We need contact information for the organization.
  - For standardization, I'd like to follow the original example map above, which collected data from [this form](https://docs.google.com/forms/d/e/1FAIpQLScL414aEv9XjLpbN6-56G4r7nFgT7htxrsQfmyiETxaFk1RLg/viewform).
  - We need a created at and last updated field for freshness.
  - We should learn how changing search parameters in Kumu affect the http requests and make a front end interface to allow users to search with specificity, though emphasis should be UX and simplicity over granularity of returns.
  
  
## Flows

Relief User --> Landing --> Select by Location --> Display Map --> Click Node for more info

Volunteer User --> Landing --> Data Entry Form --> {Validation} --> Data Entered into Object --> object uploaded to kumu

Unsure of +/- between the uncertainties in cleaning purely crowdsourced data compared to relying on data entry volunteers tasked with researching resources in a given region.


## Contributing

Halp!!!

We need folx to help on just about all aspects of this project, so hop on in!

Small note: If editing the Readme, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

[MIT © Dominick Bruno](../LICENSE)
