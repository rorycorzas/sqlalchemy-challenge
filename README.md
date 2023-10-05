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




