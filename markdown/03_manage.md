# **Starting and Managing a Data Collection Project**

### **What is project management?**
Managing a long-term research project is not merely limited to collecting data and having a careful system for backing up files---although, file management is certainly an important aspect of project management. Project management also includes monitoring the content of the data, conducting test analyses, and adjusting the research as data collection is underway. Social network users and trends are dynamic, always shifting and changing, and therefore researchers interested in conducting social network research must prepare to shift the scope of their projects while collecting data.

This chapter and the next chapter, "Developing a Research Question," are complimentary. While the "Developing a Research Question" chapter explains the importance of understanding the available data types when developing a research project, this chapter is also relevant to the development of a research question. Often, it is not until data collection begins that a more viable or sustainable research question emerges. The incoming data may encourage other questions or redirect the project entirely, and therefore properly managing a data collection means paying close attention to the data while it is collected. 

However, sometimes researchers have no specific research question at the outset of a project and are interested in collecting data because something within a social network is relevant, trending, or possibly viral. In these cases, which are frequent, scholars need to start collecting data as soon as possible for exploratory purposes (and because many trends come and go quickly). This chapter will help you start collecting data quickly, and show you effective strategies for managing long-term research projects.

**1.1 Starting a Project**

MassMine can run directly from the command line by using the `task` function. Start by using the `help` function to determine which tasks are available for MassMine. Type the following command and press ENTER:

    massmine --help=task
    
Below is another variation of this command. Both commands function the same and provide a list of the available tasks in MassMine. Type the following command and press ENTER:

    massmine -h task
    
From the list provided by the `--help` command, we will use the `twitter-search` task. This task pulls data from Twitter's Rest API, and it is a useful way to collect a small amount of historical data. Using the command below, MassMine will pull 10 recent tweets from Twitter's Rest API, and save the raw JSON data to your working directory. Your "working directory" is the location on your computer's hard drive where the terminal is currently operating. The following command is an example of how MassMine may run directly from the command line. This is only an example, do not run this command. 

    massmine --task=twitter-search --query=love --count=10 --output=love.json

Before starting to collect data, create a folder for your project. MassMine will create a basic project directory structure for you. Type the following command, but be sure to change `projectname` to the name of your data collection project and press ENTER:

    massmine --project=projectname

If you typed the command correctly, MassMine returned a new command line in the terminal. Check your working directory to see if MassMine created your project directory. You should see a new directory in your current working directory. Type in the following command and press ENTER:

    ls

*add this command to your snippets file

The command `ls` is a general command for terminals that lists files and directories within your current working directory. You will likely memorize this command quickly, but it is a good idea to save it in your snippets file along with a quick description for now.

**1.2 Running MassMine with a Configuration File**

While MassMine is designed to run directly from the command line as shown in the example above, a more sustainable method for using MassMine repeatedly is to use the `--config` task to control MassMine with a configuration file. By using a configuration file, MassMine users can easily repeat or recall a previous MassMine data collection. Using a configuration file also makes it easier to remember exactly which query was used for a previous collection, and it simplifies keeping track of data collections that are already running in the background. 

MassMine's configuration file setup takes the string of commands that operate MassMine at the terminal and places them in a single column in a text file. Therefore, the long command from above, `massmine --task=twitter-search --query=love --count=10 --output=love.json`, can be rewritten as shown in the example below. Open a new file in a text editor and type the following:

![](./images/config-example1.png)

Save the new text file in the working directory for your project, and give it the same name as your project folder. If your project folder is called `projectname` then name your file should be `projectname.txt`. Following this naming convention will allow you to easily check on your collection projects that are running in the background. We will learn how to check up on collections running in the background later in this chapter. In your terminal use the `cd` command to change your working directory to the directory for your project. Type in the following command, but be sure to change `projectname` to the name of your project and press ENTER:

    cd projectname
    
*add this command to your snippets file

The `cd` command is a general command for terminals to "change directory." By typing the name of the directory after the `cd` command, the terminal moves into the named directory as its new working directory. Like the `ls` command, you will likely memorize the `cd` command quickly, but it is a good idea to save it in your snippets file along with a quick description for now. 

Now that the terminal is working within the directory of your project, use the `ls` command to see if the config file has been saved in your project directory. Type the following command and press ENTER:

    ls
    
You should see `projectname.txt` in your project directory. This text file is the configuration file that was created in the text editor and saved in your project directory. Using MassMine's `--config` command allows this file to control MassMine. Type in the following command, but be sure to change `projectname.txt` to the name of your configuration file and press ENTER:

    massmine --config=projectname.txt
    
*add this command to your snippets file

If MassMine ran correctly, you will have seen the MassMine splash page followed by MassMine returning your terminal to a new blank command line. If you followed the directions above when creating your configuration file, then MassMine saved the collected data in the `data` directory in your project directory. Type the following command and press ENTER:

    cd data
    
This command moves your changes the terminal's working directory to the `data` directory. Use the `ls` command to see if the data was saved in the directory. Type the following command and press ENTER:

    ls

You should see a file called `mydata.json`. If you want to adjust your data collection to collect a different dataset, simply reopen the `projectname.txt` configuration file in a text editor and change the commands to match a different data type or a new query. Make sure to change the filename for the `output` to a new file name, otherwise MassMine will not run. MassMine is setup so that it will not overwrite a previous dataset. 

<!--**1.3 Managing a Long-Term Data Collection**-->

<!--![](./images/config-example2.png)-->

<!--###File conversion-->
<!--**JSON**-->
<!--The data file provided by MassMine is the raw JSON (JavaScript Object Notation). MassMine uses a tool called JSAN (Json Swiss Army kNife) to convert the raw JSON to CSV format. CSV file format is the most universally recognized format for spreadsheets data, and CSV files can be opened by any spreadsheet software. Keep in mind, however, that MassMine can collect large amounts of data, and common spreadsheet software will not work with extremely large CSV files. Later chapters explain how to use paralell processing methodologies to analyze large social network datasets, but for the earlier chapters we will work with data that can be analyzed in spreadsheet software.-->


