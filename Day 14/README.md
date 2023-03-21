# Streamlit Components

Components are third-party Python modules that extend what's possible with Streamlit [1].

## What Streamlit components are available?

There are several dozens of Streamlit components featured on Streamlit's website [2].

Fanilo (a Streamlit Creator) curated an amazing list of Streamlit components on a wiki post [3] that lists about 85 Streamlit components as of April 2022.

## How to use?

Streamlit components are just a pip-install away.

In this tutorial, let's get you started in using the streamlit_pandas_profiling component [4].

## Install the component

```
pip install streamlit_pandas_profiling
```
## Demo app

Streamlit App

## Code

Here's how to build a Streamlit app using a component:

```
import streamlit as st
import pandas as pd
import pandas_profiling
from streamlit_pandas_profiling import st_profile_report

st.header('`streamlit_pandas_profiling`')

df = pd.read_csv('https://raw.githubusercontent.com/dataprofessor/data/master/penguins_cleaned.csv')

pr = df.profile_report()
st_profile_report(pr)
```
## Line-by-line explanation

The very first thing to do when creating a Streamlit app is to start by importing the streamlit library as st as well as other libraries used in the app like so:

```
import streamlit as st
import pandas as pd
import pandas_profiling
from streamlit_pandas_profiling import st_profile_report
```
This is followed by creating a header text for the app:

```
st.header('`streamlit_pandas_profiling`')
```
Next, we load in the Penguins dataset using the read_csv command of pandas.

```
df = pd.read_csv('https://raw.githubusercontent.com/dataprofessor/data/master/penguins_cleaned.csv')
```
Finally, the pandas profiling report is generated via the profile_report() command and displayed using st_profile_report:

```
pr = df.profile_report()
st_profile_report(pr)
```
## Making your own Components

If you're interested in making your own component, please check out the following resources:

 - Create a Component
 - Publish a Component
 - Components API
 - Blog post on Components
  
Alternatively, if you prefer to learn using videos, our engineer Tim Conkling has put together some amazing tutorials:

 - How to build a Streamlit component | Part 1: Setup and Architecture
 - How to build a Streamlit component | Part 2: Part 2: Make a Slider Widget

## Further reading about Components
 1. Streamlit Components - API Documentation
 2. Featured Streamlit Components
 3. Streamlit Components - Community Tracker
 4. streamlit_pandas_profiling