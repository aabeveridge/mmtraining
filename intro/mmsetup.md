#MassMine Setup

This section is for setting up MassMine for automated data collection. Often, access to API data sources requires API credentials, and setup is necessary before MassMine can collect data. This section explains how to access the required keys and tokens that allow API access, and how to save those credentials for use in ongoing data colletion projects. The steps below are a one-time setup. Once completed, MassMine will automatically connect to the available data sources. 

**The following MassMine sources DO NOT require credentials or setup for access:**

- Wikipedia
- More coming soon...

##Twitter Access

To collect data from Twitter's API (application programming interface) users must login to their Twitter account and create a new "application." This "application" is not actually software or a computer program, but it is the access point through which MassMine collects data from Twitter. Every Twitter "application" is provided a certain amount of bandwidth (the amount of data that may be accessed over a certain period of time), and this bandwidth limits the amount of free data an "application" may access through Twitter's API. For more details on how Twitter limits data access through their API, visit the documention pages for the Twitter APIs[^1].  MassMine allows users to collect the maximum amount of data permitted by Twitter's bandwidth restrictions.

###API Access Setup

###Step 1
If you have not installed MassMine, please refer to the newest installation instructions for your operating system at [www.massmine.org](http://www.massmine.org/docs/install.html). Following installation, open a terminal and call MassMine's help feature. Type in the following command and press ENTER:

    massmine -h
    
It is important to familiarize yourself with the help feature. To use the help feature to find the <code>task</code> MassMine uses to authenticate Twitter, type in the following command and press ENTER:

    massmine -h task
    
Using this feature in MassMine shows that the correct command for Twitter authentification is:

    twitter-auth

Later in this section you will need this command to authenticate MassMine with Twitter. Minimize your Terminal window and open your Internet browser. 

###Step 2
Seting up "application" access through Twitter requires a normal Twitter account. If you already have a Twitter account, using it to collect data through Twitter's API will not affect your account. However, in order to add API access to your Twitter account, you must prove account ownership by providing your mobile telephone number. Go to your Twitter home page and click on <code>settings</code> in the drop down menu under the <code>profile and settings</code> tab. Next, click on the <code>mobile</code> side bar menu option to provide your mobile number. 

![](./intro/mobile-twit.png)

Twitter will send a text to your phone with a code in order to confirm your phone number. Follow the steps to finish confirmation. 

###Step 3
After completing mobile setup, remain logged in to your account and go to <https://apps.twitter.com>. Next, click on the <code>Create New App</code> button. On the following screen, fill in the boxes shown below. Under "Name" you will need to provide a unique application name, but "Description" and "Website" are allowed to be generic information. 

![](./intro/create-app.png)

###Step 4
After creating the "application," click on the application name and it will take you to the page for that application. In there you will click on a link in the middle of the page titled: "manage keys and access tokens."

![](./intro/keys-click.png)

After clicking on "manage keys and access tokens" link, you will be redirected to the page that provides the credentials MassMine requires in order to collect data from the Twitter APIs. Keep this page open because you will need to copy and paste the keys and tokens on this page into MassMine.

![](./intro/keys-tokens.png)

###Step 5
While keeping the keys and tokens page open in your browser, return to your terminal window and use the <code>twitter-auth</code> task as shown below. Type in the following command and press ENTER.

    massmine --task=twitter-auth
   
You will be asked: <code>Would you like to setup your Twitter credentials?</code> Answer with <code>yes</code> and press ENTER to continue. 


[^1] <https://dev.twitter.com/overview/documentation>
