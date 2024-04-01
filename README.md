# YouTube-Data-Harvesting-and-Warehousing-using-SQL-and-Streamlit
A project run the entire application through streamlit where you can collect data and store it in MongoDB. It extracts, transforms and loads the data into MYSQL and performs various SQL queries. 
To create a Streamlit application that allows users to access and analyze data from multiple YouTube channels. The application should have the following features:
1  Ability to input a YouTube channel ID and retrieve all the relevant data (Channel name, subscribers, total video count, playlist ID, video ID, likes, dislikes, comments of each video) using Google API.
2 Ability to collect data for up to 10 different YouTube channels or more and store them in the data lake by clicking a button.
3 Option to store the data in a MYSQL.
4 Ability to search and retrieve data from the SQL database using different search options, including joining tables to get channel details.

Libraries used:
sqlalchemy
pymongo
googleapiclient.discovery
pandas
streamlit
PIL

Functions:
ch_details(channel_id)
This function gets channel details like title, description, view count, video count etc using API.
v_details(channel_id)
This function gets video details like title, description, view count, comment count etc using API.
c_details(channel_id)
This function gets latest 10 comments from each video.
scrape_and_store
This function calls all the 3 above function and stores the data in MongoDB.
migrate_channel_details(channel_name_s)
This function migrates the channel details from MongoDB to MYSQL.
migrate_video_details(channel_name_s)
This function migrates the video details from MongoDB to MYSQL.
migrate_comment_details(channel_name_s)
This function migrates the comment details from MongoDB to MYSQL.
tables(channel_name)
This function calls the 3 functions above and return a message "table createed successfully".
show_channels_table()
This function displays the channel table with all the details of channels inserted so far into SQL when selected.
show_video_table()
This function displays the video table with all the details of videos of channels inserted so far into SQL when selected.
show_comment_table()
This function displays the comment table with all the details of comments under each videos of channels inserted so far into SQL when selected.

Last part of the code is the streamlit part. This runs the code in streamlit application. 
There is also a select box containing 10 questions. When you select a perticular question, a sql query runs and get you the answer.
