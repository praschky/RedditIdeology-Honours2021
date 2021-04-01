# Progress Tracker 

## Tuesday March 30

* Created user_flair_scraper_draft.py, a script which goes through the most recent posts on the PCM subreddit and looks at each comment. For each comment it records the username and user flair of the comment's author (if the comment has a flair). It saves these to a csv. 

* Created user_flair_scraper_draft.py, a script that contains a function that can record the entire post and comment history of a specified reddit user. We can loop through a list of users to create a csv file that contains the entire post/comment history of multiple users. Each row of the output csv has the following columns:
* username | interaction_type (post or comment) | title (if it is a post) | body (text) | score (of the post) | time (of creation) | subreddit


## Thursday April 1 

* Github repo created, user_flair_scraper_draft.py and user_history_scraper_draft.py uploaded to repo

* To get a sense of how long it takes to scrape user names and flairs from the comments on the posts in the PCM subreddit, I ran user_flair_scraper_draft.py  several times, each time specifying that it stop after collecting usernames and flairs for a certain number of users.
* The results are as follows: 
    * 1000 users | 71.79 seconds
    * 2000 users | 114.6 seconds
    * 3000 users | 215.34 seconds
    * 4000 users | 293.65 seconds
    * 5000 users | 368.24 seconds
    * 6000 users | 558.32 seconds
    
* Updated user_flair_scraper_draft so that it scrapes 1000 user/flair pairs at a time and then adds each user/pair as a row to an existing .csv file. This way, if the computer doing the scraping is turned off while the script is running or something else terminates the script, most of the scraped data will still be saved and available.