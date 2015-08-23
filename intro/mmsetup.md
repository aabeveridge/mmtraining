#Setup

For data sources that require API credentials, setup is necessary before MassMine can collect data. This section explains how to access the required keys and tokens that allow API access, and how to save those credentials for running MassMine at later points in time.

##Twitter

To collect data from Twitter's API (application programming interface) users must login to their Twitter account and create a new "application." This "application" is not actually software or a computer program, but it is the access point through which MassMine collects data from Twitter. Every Twitter "application" is provided a certain amount of bandwidth (the amount data that may be accessed over a certain period of time), and this bandwidth limits the amount of free data an "application" may access through Twitter's API. For more details on how Twitter limits data access through their API, visit their documention pages at [https://dev.twitter.com](https://dev.twitter.com/overview/documentation). MassMine allows users to collect the maximum amount of data permitted by Twitter's bandwidth restrictions.

###API Access Setup

####Step 1
Seting up "application" access through Twitter requires a normal Twitter account. If you already have a Twitter account, using it to collect data through Twitter's API will not affect your account. However, in order add API access to your Twitter account, you must prove account ownership by providing your mobile telephone number. Go to settings > mobile to fulfill this requirement. 

![](./intro/mobile-setup.png)

####Step 2
After completing mobile setup, go to <https://dev.twitter.com> and click on "manage apps" under the "Tools" heading at the bottom of the page:

![](./intro/manage-apps.png) 

####Step 3
Next you will click on the "Create New App" button, and then on the following screen fill in the boxes shown below. Under "Name" you will need to provide a unique application name, but "Description" and "Website" are allowed to be generic information. 

![](./intro/create-app.png)

