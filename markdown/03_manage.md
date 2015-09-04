# **Starting and Managing a Data Collection Project**

### **What is project management?**
Managing a long-term research project is not merely limited to collecting data and having a careful system for backing up files---although, file managment is certainly an important aspect of project management. Project management also includes monitoring the content of the data, conducting test analyses, and adjusting or augmenting the research as data collection is underway. Social network users and trends are dynamic, always shifting and changing, and therefore researchers interested in conducting social network research have to prepare to adjust or shift the scope of their projects while collecting data.

This section and the next section, "Developing a Reserach Question," are complimentary. While the "Developing a Research Question" section explains the importance of understanding the available data types when developing a research project, this section is also important to the process of developing a research question. Often, it is not until data collection begins that a more viable or sustainable research question emerges. The data may encourage other questions or redirect the project entirely, and therefore properly managing a data collection means paying close attention to the data while it is collected. 

However, sometimes researchers are interested in collecting data because something within a social network is relevant, trending, or possibly viral. In these cases, which are frequent, scholars do not yet have a scope or particular question for their project, and need to start collecting data as soon as possible for exploratory purposes (and because many trends come and go quickly). Social networks are a useful site for exploratoring new possibilities for social and political research, for studying the flow of information, for investigating the sharing and remixing of digital artifacts, or for understanding the composition of particular user networks.

### **What are "snippets"?**
Throughout this textbook there are directions for saving "snippets" of terminal commands or code for later use. Wikipedia defines snippets as "a programming term for a small region of re-usable source code, machine code, or text."[^1] The snippets suggested for saving from this section will be MassMine text commands and terminal commands for beginners to easily and quickly rerun MassMine. In later there are directions for saving snippets of R code for statistical analyses and data visualization. One of the most intimidating aspects of using a terminal or learning to program are the vast amount of terms, commands, syntax, and functions that must be remembered. By creating a basic workflow for saving snippets and recalling them later, the need for rote memorization is greatly reduced. Many text editors provide snippet management, and this will be addressed in later sections of this textbook. However, for this section, a simple text file for saving snippets will suffice. 

####Creating the snippets file

Open a text editor on your computer and add the following line at the top of a new text file:

    # massmine snippets
    
The `#` is a "comment" indicator common to many programming languages. Even though programming knowledge is not necessary for using MassMine to collect data, many of the conventions common to programming and reproducible research are suggested throughout the first sections of this book. 

Begin by saving a basic snippet for the help command. This snippet will use the help command to find the available tasks in MassMine:

    # massmine help command to find available tasks
    massmine --help=task
    
The first line in the snippet is a comment explaining what the command does, and the second line is the command itself. It is important to put commands on their own line to help error-proof the copying and pasting of commands. After a while, you will have many of the snippet commands memorized, but for now it is better to save important commands in your snippets file and to add descriptive comments to them. 

Minimize your snippets file, but do not close it. Throughout this section you will see `*add this command to your snippets file` after certain terminal commands. Please be sure to type the commands in the terminal first, and test them before writing them into your snippets file. It is important that you get used to typing in a terminal and that you test the commands before saving them. Also, keep in mind that terminal commands must be precise and they are case sensitive. Many errors are simply caused by typos or incorrect case. Errors are ok--do not fear breaking the computer by typing an incorrect command. If you recieve an error, double check that your command matches the instructions exactly, and then try again. 

### **1) Starting a Data Collection**

**1.1**  

MassMine can run directly from the command line by using the `task` function. Start by using the help function to determine which tasks are available for MassMine. Type the following command and press ENTER:

    massmine --help=task
    
Below is another variation of this command. Both commands function the same and provide a list of the avialable tasks in MassMine. Type the following command and press ENTER:

    massmine -h task
    
From the list provided by the `--help` command, we will use the `twitter-search` task. This task pulls data from Twitter's Rest API, and it is a useful way to collect a small amount of historical data. Using the command below, MassMine will pull 10 recent tweets from Twitter's Rest API, and save the raw JSON data to your working directory. Your "working directory" is the location on your computer's hard drive where the terminal is currently operating. Type the following command and press ENTER:

    massmine --task=twitter-search --query=love --count=10 --output=love.json

You should have seen the MassMine splash screen followed by MassMine returning your terminal back to the command line. Check your working directory to see if MassMine saved the data for you. You should see a file called `love.json` in your working directory. Type in the following command and press ENTER:

    ls

*add this command to your snippets file

The command `ls` is a general command for terminals that lists files and directories within your current working directory. You will likely memorize this command quickly, but it is a good idea to save it for now along with a quick description. 

**1.2**

The data file provided by MassMine is the raw JSON (Javascript Object Notation)
