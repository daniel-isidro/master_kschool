# Advanced Visualizations
## Sébastien Pérez, DS, Amadeus
### Vega-Lite: a Grammar of Interactive Graphics

* **Altair:** High-level API from the Vega-Lite JSON schema

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
