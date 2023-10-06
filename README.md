# sqlalchemy-challenge

Aurora Perez Corzas
Data Analysis, 2023

# Github Repository link 

https://github.com/rorycorzas/sqlalchemy-challenge.git


# Libraries in Jupyter notebook climate_starter.ipynb

%matplotlib inline
from matplotlib import style
style.use('fivethirtyeight')
import matplotlib.pyplot as plt

import numpy as np
import pandas as pd
import datetime as dt
from datetime import timedelta


import sqlalchemy
from sqlalchemy.ext.automap import automap_base
from sqlalchemy.orm import Session
from sqlalchemy import create_engine, func
from sqlalchemy import inspect
from sqlalchemy import select

# Background

Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii. To help with your trip planning, you decide to do a climate analysis about the area. The following sections outline the steps that you need to take to accomplish this task. 

This task will be divided into the next parts:

# Part 1: Analyze and Explore the Climate Data

In this section, you’ll use Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database. Specifically, you’ll use SQLAlchemy ORM queries, Pandas, and Matplotlib.

This part is contained in file named: climate_starter.ipynb

The resulting plots are in folder:  /Images/
Precipitation_1year.png
YearlyTOBS.png

Important: Remember to close your session at the end of your notebook.

# Part 2: Design Your Climate App

Now that you’ve completed your initial analysis, you’ll design a Flask API based on the queries that you just developed

Note: When you run app.py from Visual Studio Code, left click + Ctrl on file name > Run Python file in terminal. Then you will be able to open a chrome browser on http://127.0.0.1:5000, and change between the 
routes defined in the api. 

# Output when you Run Python file in terminal

(dev) auroracorzas@192 sqlalchemy-challenge % /Users/auroracorzas/anaconda3/envs/dev/bin/python /Users/auroracorzas/Documents/GitHub/sqlalchemy-challenge/app.py
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
 * Restarting with watchdog (fsevents)
 * Debugger is active!
 * Debugger PIN: 173-226-790
127.0.0.1 - - [06/Oct/2023 14:19:45] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [06/Oct/2023 14:19:52] "GET /api/v1.0/start HTTP/1.1" 200 -
127.0.0.1 - - [06/Oct/2023 14:20:25] "GET /api/v1.0/2016-08-23 HTTP/1.1" 200 -
Exception during reset or similar

# Part of app.py code with available routes defined

@app.route("/") # / main url
def welcome():
    return (
        f"Available Routes:<br/>"
        f"/api/v1.0/precipitation<br/>"
        f"/api/v1.0/stations<br/>"
        f"/api/v1.0/tobs<br/>"
        f"/api/v1.0/start<br/>"
        f"/api/v1.0/start/end<br/>"
    )

To access each one simply add the termination to the http://127.0.0.1:5000

Like this:
http://127.0.0.1:5000/api/v1.0/precipitation
http://127.0.0.1:5000/api/v1.0/stations

In the case of tobs, it is defined a constant to pick the info from this particular TOBS = 'USC00519281'
http://127.0.0.1:5000/api/v1.0/tobs

And when you want to look for a particular date in this two links you must declare in url which date you want the json information in format (YYYY-MM-DD)
http://127.0.0.1:5000/api/v1.0/start
http://127.0.0.1:5000/api/v1.0/start/end

For example: 
http://127.0.0.1:5000/api/v1.0/2016-08-23
http://127.0.0.1:5000/api/v1.0/2016-08-23/2016-10-23

# Important: DO NOT forget to CLOSE all open sessions in browser and terminal

Happy life!





