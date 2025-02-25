# Reddit API Project

## Overview
This project contains Python scripts that interact with the Reddit API to fetch various data from subreddits.

## Requirements
- Python 3.4.3 or higher
- Ubuntu 20.04 LTS
- Requests module

## Files and Functions
- **0-subs.py**: Function to get the number of subscribers for a subreddit
- **1-top_ten.py**: Function to print the titles of the top 10 hot posts for a subreddit
- **2-recurse.py**: Recursive function to get all hot posts for a subreddit
- **100-count.py**: Advanced function to count specified keywords in hot post titles

## Usage
```
# Get subscriber count
python3 0-main.py programming

# Get top 10 hot posts
python3 1-main.py programming

# Get all hot posts
python3 2-main.py programming

# Count keywords in hot posts
python3 100-main.py programming 'python java javascript'
```

## Author
Shighi
