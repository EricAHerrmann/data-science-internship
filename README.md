# data-science-challenge README

Included in this Repo are solution files for data science internship challenge.

Table of Contents: |Details|
:-------------------|:-------------
**input_data.py**|  the original input data |
**Python Notebook Files (2):** | Part 1  -  the solution file for Part 1 of the challenge|
||Part 2  -  the solution file for Part 2 of the challenge|
**users.py** | the output from Part 1, a collection of dictionaries containing each user (identified by user_id) and the number of times they interacted with a certain event |
**PNG image files (3):** | The plots created by Part 2, each representing a data visualization relating to the data on PhotoUpload interactions |
**PDF Write Up (1)** |


README cont'd: 

**The Problem:** Tasked with creating a data structure which keeps track of the number of times a user triggered each possible event. Technical requirement that the programming solution did not "hardcode" the possible names of the events beforehand. Instead, the code was required to be flexible and accept any event names present in the input file or any future input file. Technical requirement that the solution only rely on Python's Standard Library. The second problem was to create a histogram of users bucketed by how many times they triggered 'PhotoUpload'. The technical requirements for this problem specified that additional libraries were acceptable in the solution. 

**The Solution:** Part 1 was developed in a Python Notebook (ipynb). Began by importing the data as a collection of dictionaries. Iterated through the data once to create an array of each user ID and each event name associated with each event log. Created an array of possible event types by removing duplicates from the event names array. Generated a dictionary for each user (identified by "user_id"), and added keys for each event type, initialized the event count to zero. This collection of dictionaries has keys for each user's ID and the amount of times each user triggered each event. Iterated over the input data once again to increase the count for the event value for a user if their ID matched the ID in the log. Finally, error checked, by ensuring that the total amount of logs in the input data was the same as the total count of each user summated. The final collection of dictionaries was written into 'users.py'.

Part 2 was also developed in a Python Notebook. I began by doing as the problem asked me by using Matplotlib.pyplot to generate a histogram of users bucketed by how many times they triggered the 'PhotoUpload' event. This plot was saved as 'numUsers_x_numPhotoUploads(Total).png'. I noticed that the majority of users had never triggered the 'PhotoUpload' event, so this histogram was limited in readability. I generated a second histogram excluding users who never triggered the 'PhotUpload' event. This histogram was saved as 'numUsers_x_numPhotoUploads(NonZero).png'. The heights of each bar were scaled automatically to improve readablity. Finally, I generated a third plot, a scatter graph, which represents the relationship between number of 'PhotoUpload' events triggered by each user and the number of Total Event Interactions triggered by this user. The number of Total Event Interactions is simply a sum of the count for each event type by user, including (in this case) 'GuideDownload', 'GuideSession', 'ConnectionRequested', and 'PhotoUpload'. This plot was saved as 'numPhotoUploads_x_numTotalInteracts.png'. I adjusted the alpha down to 0.2 for the data points in this plot better create a sense of density. Finally, I adjusted each of the plots to match (as close as I could) the color of GuideBook's branding to ensure on-brandness. These three plots are more visual than numerical. One shortcoming of my work is a lack of a best fit line for the scatter plot, with appropriate R value. This would have been valuable information to include, but for the purpose of making brief generalizations about the data, I regarded that feature as ultimately uncessecary. The relationships presented in the date overall seem apparent on the surface level and the plots serve as solid visualizations of the data. 



