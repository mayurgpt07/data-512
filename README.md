# data-512
## Assignment-1: Data Curation
For the purpose of the assignment we combine the data about Wikipedia page traffic from two different API's into a single dataset, perform some simple data processing steps on the data and analyze the data

### Wikipedia API
The Wikipedia page traffic API is split into two seperate endpoints based on the date as:
1) **Legacy Pagecounts API** - [Documentation]() and [Endpoints]() provides access to desktop and mobile traffic data from December 2007 through July 2016. <br />
  a) **API Method** - GET <br />
  b) **API Endpoint** - https://wikimedia.org/api/rest_v1/metrics/legacy/pagecounts/aggregate/{project}/{access-site}/{granularity}/{start}/{end} <br />

2) **Pageviews API** - [Documentation]() and [Endpoints]() provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month. <br />
  a) **API Method** - GET <br />
  b) **API Endpoint** - https://wikimedia.org/api/rest_v1/metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end} <br />

#### Note
* There is an overlap of about 1 year in the data from both the API's <br />
* The Pagecounts Wikipedia API gives the count for all kinds of agent (including users, crawlers, bots etc) <br />
* The Pageviews Wikipedia API gives the count for all kinds of agent (including users, crawlers, bots etc) but we are gathering data for **users only** <br />

### Consolidated Data Description
* **year** - Year(YYYY) of the page view
* **month** - Month(MM) of the page view
* **pagecount_all_views** (C) - Count of views on any page from any device in the date range 2008-01-01 to 2016-07-30
* **pagecount_desktop_views** (C) - Count of views on any page from desktop website in the date range 2008-01-01 to 2016-07-30
* **pagecount_mobile_views** (C) - Count of views on any page from either mobile website or mobile app in the date range 2008-01-01 to 2016-07-30
* **pageview_all_views** (V) - Count of views on any page from any device in the date range 2015-07-01 to 2020-09-30
* **pageview_desktop_views** (V) - Count of views on any page from desktop website in the date range 2015-07-01 to 2020-09-30
* **pageview_mobile_views** (V) - Count of views on any page from either mobile website or mobile app in the date range 2015-07-01 to 2020-09-30
(C) - column data source is Legacy Pagecounts API <br />
(V) - column data source is Pageviews API

### Steps to run
