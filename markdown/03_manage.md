# **Starting and Managing a Data Collection Project**

### **What is project management?**
Managing a long-term research project is not merely limited to collecting data and having a careful system for backing up files---although, file managment is certainly an important aspect of project management. Project management also includes monitoring the content of the data, conducting test analyses, and adjusting or augmenting the research as data collection is underway. Social network users and trends are dynamic, always shifting and changing, and therefore researchers interested in conducting social network research have to prepare to adjust or shift the scope of their projects while collecting data.

This section and the next section, "Developing a Reserach Question," are complimentary. While the "Developing a Research Question" section explains the importance of understanding the available data types when developing a research project, this section is also important to the process of developing a research question. Often, it is not until data collection begins that a more viable or sustainable research question emerges. The data may encourage other questions or redirect the project entirely, and therefore properly managing a data collection means paying close attention to the data while it is collected. 

However, sometimes researchers are interested in collecting data because something within a social network is relevant, trending, or possibly viral. In these cases, which are frequent, scholars do not yet have a scope or particular question for their project, and need to start collecting data as soon as possible for exploratory purposes (and because many trends come and go quickly). Social networks are a useful site for exploratoring new possibilities for social and political research, for studying the flow of information, for investigating the sharing and remixing of digital artifacts, or for understanding the composition of particular user networks.

### **What are "snippets"?**
Throughout the text below you will be encouraged to save "snippets" of text commands for later use. Wikipedia defines snippets as "a programming term for a small region of re-usable source code, machine code, or text."[^1] The snippets that you will save from this section will be MassMine text commands for the terminal that you will need to remember at a later point in time. In later chapters you will save snippets of R code for statistical analyses. One of the most intimidating aspects of using a terminal or learning to program is the vast amount of terms, commands, syntax, and functions that must be remembered. By creating a basic workflow for saving snippets and recalling them later, the need to memorize is greatly reduced. Many text editors provide snippet management, and this will be addressed in later sections of this textbook. However, for this section, a simple text file for saving snippets will be adequate. 

####Create the snippets file

Open a text editor on your computer and add the following line at the top:

    # massmine snippets
    


### **1) Starting a Data Collection**

**1.1**  

MassMine can run directly from the command line by using the `task` function. Start by using the help function to determine which tasks are available for MassMine. Type the following into MassMine and press ENTER:

    massmine --help=task
    
Below is another variation of this command. Both commands function the same and provide a list of the avialable tasks in MassMine. Type the following into MassMine and press ENTER:

    massmine -h task

If MassMine has already been authenticated with Twitter, then you can run a small test data collection with the command below. With this command MassMine will pull 10 recent tweets from Twitter's Rest API, and save the raw JSON data to your working directory. Your "working directory" is the location on your computer's hard drive where the terminal is currently running. Type the following command to see the contents of that "directory":

    ls

If the "directory" or "folder" is empty, then the terminal will return another blank line. Otherwise, you should see a list of the files and other directories contained with your current working directory. 

