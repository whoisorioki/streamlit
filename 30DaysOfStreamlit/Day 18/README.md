# st.file_uploader

st.file_uploader displays a file uploader widget [1].

By default, uploaded files are limited to 200MB. You can configure this using the server.maxUploadSize config option. For more info on how to set config options, see [2].

## Demo app

Streamlit App

## Code

Here's how to use st.file_uploader:

```
import streamlit as st
import pandas as pd

st.title('st.file_uploader')

st.subheader('Input CSV')
uploaded_file = st.file_uploader("Choose a file")

if uploaded_file is not None:
  df = pd.read_csv(uploaded_file)
  st.subheader('DataFrame')
  st.write(df)
  st.subheader('Descriptive Statistics')
  st.write(df.describe())
else:
  st.info('☝️ Upload a CSV file')
```
## Line-by-line explanation

The very first thing to do when creating a Streamlit app is to start by importing the streamlit library as st and other prerequisite library like so:

```
import streamlit as st
import pandas as pd
```
This is followed by creating a title text for the app:

```
st.title('st.file_uploader')
```
Next, we'll use st.file_uploader to display a file uploader widget for accepting user input file:

```
st.subheader('Input CSV')
uploaded_file = st.file_uploader("Choose a file")
```
Finally, we define conditional statements for initially displaying a welcome message inviting users to upload their file (as implemented in the else condition). Upon file upload, the if statements are activated and the CSV file is read by the pandas library and displayed via the st.write command.

```
if uploaded_file is not None:
  df = pd.read_csv(uploaded_file)
  st.subheader('DataFrame')
  st.write(df)
  st.subheader('Descriptive Statistics')
  st.write(df.describe())
else:
  st.info('☝️ Upload a CSV file')
```
## Further reading
 - st.file_uploader
 - Set configuration options