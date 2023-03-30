# st.selectbox

st.selectbox allows the display of a select widget.

## What we're building?

A simple app that asks the user what their favorite color is.

Flow of the app:

 1. User selects a color
 2. App prints out the selected color

## Demo app

The deployed Streamlit app should look something like the one shown in the below link:

Streamlit App

## Code
Here's the code to implement the above mentioned app:

```
import streamlit as st

st.header('st.selectbox')

option = st.selectbox(
     'What is your favorite color?',
     ('Blue', 'Red', 'Green'))

st.write('Your favorite color is ', option)
```
## Line-by-line explanation

The very first thing to do when creating a Streamlit app is to start by importing the streamlit library as st like so:

```
import streamlit as st
```
This is followed by creating a header text for the app:

```
st.header('st.selectbox')
```
Next, we will create a variable called option that will accept user input in the form of a select input widget via the st.selectbox() command.

```
option = st.selectbox(
     'What is your favorite color?',
     ('Blue', 'Red', 'Green'))
```
As we can see from the above code box, the st.selectbox() command accepts 2 input arguments:

 1. The text that goes above the select widget, i.e. 'What is your favorite color?'
 2. The possible values to select from ('Blue', 'Red', 'Green')
Finally, we'll print out the selected color as follows:

```
st.write('Your favorite color is ', option)
```
## Next steps

Now that you have created the Streamlit app locally, it's time to deploy it to Streamlit Community Cloud.

References
More about st.selectbox