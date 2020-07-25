# Advanced Visualizations
## Sébastien Pérez, DS, Amadeus
### Altair

* **Altair:** Altair is a declarative statistical visualization library for Python, based on Vega and Vega-Lite, and the source is available on GitHub

* When using Altair, always copy and paste column names from ```dataframe.columns```

* In Altair, you cannot export images into a fodler (unlike in matplotlib, with ```plt.savefig('image.png')```)

* For working with large datasets in Altair, use groupby:

```python
temp = weather_df.groupby('country').mean().reset_index()

alt.Chart(temp).mark_bar().encode(
    x='country',
    y='mean(temp)'
)
```

* When working with maps, you need to give a TopoJSON URL to Altair for drawing the countries/cities/neighborhoods

* We can also work with the ```folium``` library for maps

* Themes in Altair are configured with a config dictionary

### DRAW SVG

```python
!pip install drawSvg
```

* DRAW SVG is a free online drawing editor with additional tools for generating, optimizing, converting your drawings and sharing them with a community.

### Streamlit

* It has revolutionized the way DS present their work, as it removes the need of programming web services and web pages

* It can be run locally, but if used on Google Colab the Streamlit server can be accessed with the mobile phone

* We can use ```ngrok``` to tunnel the Streamlit server, that is blocked from the outside of the Google Colab servers, so it can be accessed from the internet

* ```streamlit``` can only run the code in one .py file

