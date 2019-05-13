---
title: "The Learning Analytics API (LA-API)"
permalink: /tools/LA-API/
---

The LA-API is an emerging project in delivering learning analytics over an ecosystem of services. It is designed to facilitate the building of scalable LA Infrastructure, keeping data capture separate from analytics and reporting. This is achieved by the careful use of an extensible [GraphQL schema](https://graphql.org/), which enables the flexible mutation of data as required by various learning analytics tools that consume that data.

![The LA-API]({{site.baseurl}}/assets/images/LA-APIv2.jpg)

The development of the LA-API was initially supported by the Australian Government's Office for Learning and Teaching (OLT), under a Research and Innovation grant (Enabling connected learning via open source analytics in the wild: learning analytics beyond the LMS). Since then significant internal funds and support have been provided by UTS.

### Pragmatic data Interoperability

Key to the functionality of the LA-API is a new approach to achieving data interoperability. Instead of requiring the adoption of standards (which is rarely followed by practitioners) we are taking a more flexible approach, one which makes it easier to use data in LA infrastructure if data standards are followed, but which can be extended as necessary. This is facilitated by the use of of resolver functions in the GraphQL, which can be mapped to various data sources as necessary to accommodate new sources. If a data source follows a best practice adoption of a data standard then it is more likely to already be mapped in the GraphQL implementation. But if a LA group insists on doing things "their own way" then they can propose a new extension.

### Code bases

There are a number of repositories associated with this data pipeline. All are released open source  (including the [CLA toolkit]({{site.baseurl}}/tools/CLAtoolkit/) which collects social media data about student participation in defined learning activities beyond the LMS).

- [https://github.com/uts-cic/canvas-extract](https://github.com/uts-cic/canvas-extract)
- [https://github.com/uts-cic/lrs-mongo](https://github.com/uts-cic/lrs-mongo)
- [https://github.com/uts-cic/graphql-la-api](https://github.com/uts-cic/graphql-la-api)
- [https://github.com/uts-cic/dashboards-la-api](https://github.com/uts-cic/dashboards-la-api)
- [https://github.com/uts-cic/xAPI-profiles](https://github.com/uts-cic/xAPI-profiles)

A number of other tools will be interfaced with the LA-API. In the first case these are tools developed by [UTS:CIC](https://utscic.edu.au/).

### Contributing

If you are interested in contributing to this LA infrastructure project then you could fork and propose changes to the GraphQL schema being used by the LA-API, ([see the repo](https://github.com/uts-cic/la-graphql-api)). Feel free to [contact us](mailto:kirsty.kitto@uts.edu.au) if you would like to get more information about this project.
