---
title: "xAPI Analytics - Stepping out of the LRS (Part 1)"
description: "Using opensource tools to build custom dashboards and reports for xAPI data"
categories:
  - Blog
tags: [xAPI, learning analytics, dashboards, reports, LRS]
author: aneesha
---


xAPI statements are stored in a Learning Record Store (LRS). The API specification defines how statements are inserted and provides a very basic way to retrieve statements. The specification does not define anyway to query the LRS across all stored fields or return aggregate counts. Various LRS implementations exist and most use a database as a backend, Learning Locker for example uses MongoDB. The underlying database technology used in most LRS implementations supports ad-hoc querying and this allows LRS vendors to build reporting and data warehousing capabilities. The xAPI specification however only requires that full statements are returned and that a link, available for 24 hours remains for access to the queried data which can then be traversed over (if multiple pages) to obtain the statements for further processing and analysis. This is understandable as the LRS is middleware and contains an enormous amount of data making ad-hoc querying inefficient.  Data needs to be extracted and transformed into a data warehouse for advanced analytics. LRS vendors such as WaxLRS and YetAnalytics are already providing analytics in their products.  The xAPI community however needs to share ideas on creating custom dashboards, reports and advanced analytics. This has been the main driver behind writing a series of blog posts on “Stepping out of the LRS”.

In the “Stepping out of the LRS” series of blog posts, open source tools will be used to build analytics for xAPI statements extracted from an LRS. The focus will be on using open source tools to:

- ingest and expose the xAPI statements for aggregate queries
- build a configurable dashboard 
- encourage experimentation with open source log processing and dashboard visualisation tools

In Part 2, xAPI statements will be stored in Postgres with a dashboard built in <a href="http://redash.io/">Re:Dash</a>. Postgres is a relational database with excellent support for storing and querying json documents. ReDash is a unique dashboard application build in Python and Django. Re:Dash is able to store queries and then display the results in a variety of widgets.

In Part 3, xAPI statements will be stored in <a href="https://www.elastic.co/products/elasticsearch">ElasticSearch</a> with a dashboard provided by <a href="https://www.elastic.co/products/kibana">Kibana</a>. ElasticSearch and Kibana are used extensively for log file processing.
