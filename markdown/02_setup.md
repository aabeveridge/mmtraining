# **API Authentification**

This section is for setting up MassMine for automated data collection. Often, API data sources require API credentials, and setup is necessary before MassMine can be authorized to collect data. This section explains how to access the required keys and tokens that allow API access, and how to save those credentials for use in ongoing data colletion projects. The steps below are a one-time setup. Once completed, MassMine will automatically connect to the available data sources for collection projects. 

**The following MassMine sources DO NOT require credentials or setup for access:**

- Wikipedia
- More coming soon...

##Twitter Authentification

To collect data from Twitter's APIs (application programming interfaces) you must login to your Twitter account and create a new "application." This "application" is not actually software or a computer program, but it is the access point through which MassMine collects data from Twitter. Every Twitter "application" is provided a certain amount of bandwidth[^1], and this limits the amount of free data an "application" may access through Twitter's API. For more details on how Twitter limits data access through their API, visit the documention pages for the Twitter APIs[^2].  MassMine assists users in collecting the maximum amount of data permitted by Twitter's bandwidth restrictions.

### **1) MassMine Help**

**1.1**  
If you have not installed MassMine, please refer to the newest installation instructions for your operating system at [www.massmine.org](http://www.massmine.org/docs/install.html). After MassMine has been installed, open a terminal and call MassMine's help feature. 

Type in the following command into the terminal and press ENTER:

    massmine --help
    
MassMine also accepts the short form version of the help command:

    massmine -h

All of MassMine's commands have a short form version, but for the sake of clarity the longer form commands will be used. 
    
**1.2**  
It is important to familiarize yourself with the help feature. To use the help feature to find the `task` MassMine uses to authenticate Twitter, type in the following command and press ENTER:

    massmine --help=task
    
Using this feature in MassMine shows that the correct command for Twitter authentification is:

    twitter-auth

Later in this section you will need this command to authenticate MassMine with Twitter. 

**1.3**  
Minimize your Terminal window and open your Internet browser. 

### **2) Creating an Application**

**2.1**  
Seting up "application" access through Twitter requires a normal Twitter account. If you already have a Twitter account, using it to collect data through Twitter's API will not affect your account. However, in order to add API access to your Twitter account, you must prove account ownership by providing your mobile telephone number. Go to your Twitter home page and click on `settings` in the drop down menu under the `profile and settings` tab. 

**2.2**  
Next, click on the `mobile` side bar menu option to provide your mobile number. 

***

![](./images/mobile-twit.png)

***

Twitter will send a text to your phone with a code to confirm your phone number. Follow the steps provided by Twitter to finish confirmation. 

### **3: Application Setup**

**3.1**  
After completing mobile verification, remain logged in to your account and go to <https://apps.twitter.com>, and click on the `Create New App` button. 

**3.2**  
On the following screen, fill in the boxes shown below. Under "Name" you will need to provide a unique application name, but "Description" and "Website" are allowed to be generic information.

***

![](./images/create-app.png)

***

### **4) Application Secrets and Tokens**

**4.1**  
After creating the "application," click on the application name and it will take you to the page for that application. In there you will click on a link in the middle of the page titled: "manage keys and access tokens."

***

![](./images/keys-click.png)

***

**4.2**  
After clicking on "manage keys and access tokens" link, you will be redirected to the page that provides the credentials MassMine requires in order to collect data from the Twitter APIs. Keep this page open because you will need to copy and paste the keys and tokens on this page into MassMine.

***

![](./images/keys-tokens.png)

***

### **5) Saving Application Secrets and Tokens in MassMine**

**5.1**  
While keeping the keys and tokens page open in your browser, return to your terminal window and use the `twitter-auth` task as shown below. Type in the following command and press ENTER:

    massmine --task=twitter-auth
   
**5.2**  
You will be asked: `Would you like to setup your Twitter credentials?` Answer with `yes` and press ENTER to continue. 

**5.3**  
Next you will be asked to enter your `Consumer Key`. Return to your browser window as shown in last image example above. Copy the consumer key from the webpage, paste it back in your terminal, and then press ENTER. 

**5.4**  
Follow the same process from Step 5.3 for the `Consumer Secret`, `Access Token`, and `Access Token Secret`. Once you have finished copying the 4 secrets and tokens into MassMine, you will see `Authentification setup finished!`. 


***

[^1]: "Bandwidth" is the amount of data that may be accessed over a specified period of time
[^2]: <https://dev.twitter.com/overview/documentation>
