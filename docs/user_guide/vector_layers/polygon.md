```{code-cell} ipython3
---
nbsphinx: hidden
---
import folium
```

## Polygon

```{code-cell} ipython3
m = folium.Map(location=[35.67, 139.78], zoom_start=13)

locations = [
    [35.6762, 139.7795],
    [35.6718, 139.7831],
    [35.6767, 139.7868],
    [35.6795, 139.7824],
    [35.6787, 139.7791],
]

folium.Polygon(
    locations=locations,
    color="blue",
    weight=6,
    fill_color="red",
    fill_opacity=0.5,
    fill=True,
    popup="Tokyo, Japan",
    tooltip="Click me!",
).add_to(m)

m
```

```{code-cell} ipython3
locations = [
    [
        [7.577794326946673, 8.998503901433935],
        [7.577851434795945, 8.998572430673164],
        [7.577988491475764, 8.998652380403087],
        [7.578105560723088, 8.998426807051544],
        [7.577891409660878, 8.998289750371725],
        [7.577794326946673, 8.998503901433935],
    ],
    [
        [7.578139824893071, 8.999291979141560],
        [7.578359687549607, 8.999414759083890],
        [7.578456769364435, 8.999266281014116],
        [7.578471046101925, 8.999197181604700],
        [7.578247331649095, 8.999094883721964],
        [7.578139824893071, 8.99929197914156],
    ],
    [
        [7.577851730672876, 8.997811268775080],
        [7.578012579816743, 8.997460464828633],
        [7.577798113991832, 8.997311104523930],
        [7.577667902951418, 8.997663440915119],
        [7.577851730672876, 8.997811268775080],
    ],
    [
        [7.578562417221803, 8.999551816663029],
        [7.578688052511666, 8.999654609172921],
        [7.578813688700849, 8.999443313458185],
        [7.578670920426703, 8.999369073523950],
        [7.578562417221803, 8.999551816663029],
    ],
    [
        [7.577865711533433, 8.998252059784761],
        [7.577989601239152, 8.998002756022402],
        [7.577648754586391, 8.997784460884190],
        [7.577545911714481, 8.998069316645683],
        [7.577865711533433, 8.998252059784761],
    ],
]

m = folium.Map(location=[7.577798113991832, 8.997311104523930], zoom_start=16)

folium.Polygon(
    locations=locations,
    smooth_factor=2,
    color="crimson",
    no_clip=True,
    tooltip="Hi there!",
).add_to(m)

m
```