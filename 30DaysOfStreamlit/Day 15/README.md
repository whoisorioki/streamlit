# st.latex

st.latex display mathematical expressions formatted as LaTeX.

## What we're building?

A simple app that displays a mathematical equation using LaTeX syntax via the st.latex command.

## Demo app

Streamlit App

## Code

Here's how to use st.latex:

```
import streamlit as st

st.header('st.latex')

st.latex(r'''
     a + ar + a r^2 + a r^3 + \cdots + a r^{n-1} =
     \sum_{k=0}^{n-1} ar^k =
     a \left(\frac{1-r^{n}}{1-r}\right)
     ''')
```
## Line-by-line explanation

The very first thing to do when creating a Streamlit app is to start by importing the streamlit library as st like so:

```
import streamlit as st
```
This is followed by creating a header text for the app:

```
st.header('st.latex')
```
Next, we're displaying the mathematical equation via st.latex:

```
st.latex(r'''
     a + ar + a r^2 + a r^3 + \cdots + a r^{n-1} =
     \sum_{k=0}^{n-1} ar^k =
     a \left(\frac{1-r^{n}}{1-r}\right)
     ''')
```
## References

 - Read more about st.latex in the Streamlit API Documentation.