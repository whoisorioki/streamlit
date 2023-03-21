# st.progress

st.progress displays a progress bar that updates graphically as the iteration progresses.

## Demo app

Streamlit App

## Code

Here's how to use st.progress:

```
import streamlit as st
import time

st.title('st.progress')

with st.expander('About this app'):
     st.write('You can now display the progress of your calculations in a Streamlit app with the `st.progress` command.')

my_bar = st.progress(0)

for percent_complete in range(100):
     time.sleep(0.05)
     my_bar.progress(percent_complete + 1)

st.balloons()
```
## Line-by-line explanation

The very first thing to do when creating a Streamlit app is to start by importing the streamlit library as st along with the time library like so:

```
import streamlit as st
import time
```
Next, we create a title text for the app:

```
st.title('st.progress')
```
An About box is created using st.expander and description is displayed via st.write:

```
with st.expander('About this app'):
     st.write('You can now display the progress of your calculations in a Streamlit app with the `st.progress` command.')
```
Finally, we define a progress bar and instantiate it with a starting value of 0. Then, a for loop will iterate from 0 until 100 is reached. In each iteration, we use time.sleep(0.05) to allow the app to wait for 0.05 before adding a value of 1 to the my_bar progress bar and in doing so the graphical display of the bar increases with each iteration.

```
my_bar = st.progress(0)

for percent_complete in range(100):
     time.sleep(0.05)
     my_bar.progress(percent_complete + 1)

st.balloons()
```

## Further reading
 - st.progress