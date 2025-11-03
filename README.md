

# Overview

This assignment demonstrates how to use the PRAW Reddit API wrapper to extract data from posts from multiple subreddits and export to a single csv file. We establish a connection to the Reddit API by loading our credentials. We then create functions that extract data from posts that are found either in the "hot" section of a user-specified subreddit, or by searching a user-specified keyword within any subreddit. The individual csv's created from these functions can be used as is, but further down we create individual dataframes from these csv's, concatenate these dataframes into a single dataframe containing all extracted post data, and turn this comprehensive dataframe into a final csv. We have a total of 11 csv's, 10 individual and 1 collective.

## How to Run

Prerequisites: Python 3.8+

Installation: requirements.txt file provided, in code enter: "pip install -r requirements.txt" <- This will install more than is necessary to run everything below

Configuration using provided reddit.env as template:

1.  Create a Reddit account (write down both username and password*, username is different than displayname)
2.  Go to https://www.reddit.com/prefs/apps
3.  Click "create another app..."
4.  Choose script as app type
5.  In reddit.env, replace "YOUR_CLIENT_ID_HERE" with the sequence of characters under "personal use script" in the top left corner after the app has been created.
6.  In reddit.env, replace "YOUR_CLIENT_SECRET_HERE" with the sequence of characters next to "secret."
7.  In reddit.env, set the username and password*.
8.  In reddit.env, set the redirect uri as "https://localhost:8080"
9.  In reddit.env, replace "YOUR_USER_AGENT_HERE" with "_________/1.0 by __________"  
	(replace __ with appname and username, respectively)

## Execution

Download raw .ipynb file on GitHub repository and run on Anaconda Jupyter Notebook or Google Colab

## Output

The output file, reddit_data.csv, consists of extracted data from posts from the hot section of a multiple subreddits, as well as data from posts yielded by a specific search term within a subreddit.

## Output Columns

Title - Title of extracted post

Score - Number of upvotes on post

Upvote Ratio - Percentage of upvotes out of all votes on post

Number of Comments - Number of comments on post

Author - Username of poster

Subreddit - Subreddit post is found in

URL - URL that post links to, unless the post consists entirely of text, then it is permalink

Permalink - Permalink for post

Post ID - Unique ID for post, also found within permalink

Created UTC - Time of submission in Unix Time

Selfpost? - TRUE if post consists only of text with no link to another website, FALSE otherwise

Selftext - text making up the body of the post

Post Flair - Flair applied to post

Domain - Domain of linked content


