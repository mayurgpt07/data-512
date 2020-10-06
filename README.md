# data-512
## Assignment-1: Data Curation
For the purpose of the assignment we combine the data about Wikipedia page traffic from two different API's into a single dataset, perform some simple data processing steps on the data and analyze the data

### Data Sources
The Wikipedia page traffic API is split into two seperate endpoints based on the date as:
1) **Legacy Pagecounts API** - [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts) and [Endpoints](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end) provides access to desktop and mobile traffic data from December 2007 through July 2016. <br />
  a) **API Method** - GET <br />
  b) **API Endpoint** - https://wikimedia.org/api/rest_v1/metrics/legacy/pagecounts/aggregate/{project}/{access-site}/{granularity}/{start}/{end} <br />

2) **Pageviews API** - [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) and [Endpoints](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month. <br />
  a) **API Method** - GET <br />
  b) **API Endpoint** - https://wikimedia.org/api/rest_v1/metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end} <br />

The documentations is available under [Creative Commons Attribution-ShareAlike License](https://creativecommons.org/licenses/by-sa/3.0/) <br />
See [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use) for details.

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
Follow the steps to successfully execute the jupyter notebook:
1) Download the folder **data-512-a1**
2) Unzip the folder if you have downloaded from github (no need to unzip if you have cloned the repository on your system)
3) Change directory to **data-512-a1** (cd data-512-a1)
4) Using Command Line on Windows or Terminal on Mac/Linux run the command **jupyter notebook**
5) The command will open a URL similar to ***http://localhost:8888/tree*** in your default browser (The port 8888 might change if it is already occupied)
6) You will be able to see all files of the folder **data-512-a1**
7) Double click on the file **Assignment1.ipynb** to open it
8) The jupyter notebook is up and running now
9) You can execute the notebook by running (Shift + Enter) each cell **sequentially**  or use **Kernel >> Restart & Run all**


### Additional Details
* There is an overlap of about 1 year in the data from both the API's <br />
* The Pagecounts Wikipedia API gives the count for all kinds of agent (including users, crawlers, bots etc) <br />
* The Pageviews Wikipedia API gives the count for all kinds of agent (including users, crawlers, bots etc) but we are gathering data for **users only** <br />
