# Some boxes here and there

<div style="background: linear-gradient(83deg,#7cd5ff,#a6fbca 33%,#fff37c 66%,#ffa49d)">
Test
</div>

## Common Box
This box is mostly meant as a shared template for other functions to be calling.
While it can be used individually, users should strongly consider relying on other functions.

The `_common_box` method creates two rectangles, one for the heading and one for the body of the box.
Both are optional and can be left out.
This box also automatically considers the currently defined [theme](themes) and styles the box accordingly.
```typst
_common_box(
    body: [none] [content],
	heading: [none] [content],
	body_color: [none] [color],
	body_background: [none] [color],
	heading_color: [none] [color],
	heading_background: [none] [color],
	stretch_to_bottom: false,
	bottom_box: false,
) --> [content]
```

| Argument | Type | Description |
| --- | --- | --- |
| `heading` | [content] | The upper rectangle which defines the heading of the box.
| `body` | [content] | The lower rectangle containing the body of the box. |
| `body_color` | [none],[color] | Text color of the body. |
| `body_background` | [none],[color] | Background color of the body. |
| `heading_color` | [none],[color] | Text color of the heading. |
| `heading_background` | [none],[color] | Background color of the heading. |
| `stretch_to_bottom` | [bool] | The vertical size of the box is stretched such that it fills out the remainder of the vertical space. |
| `bottom_box` | [bool] | The box should be aligned towards the bottom of the page. |

### Example
```typst
#_common_box(
    heading: "typst-posters - Create scientific posters",
)
```

## Column Box
```typst
column_box(
	body,
	..args
) --> [content]
```
| Argument | Type | Description |
| --- | --- | --- |
| `body` | [content] | 

## Bottom Box
```typst
bottom_box(
    content,
    text_relative_width: 70%,
    logo: none,
    ..args
) --> [content]
```

## Bibliography Box
```typst
bibliography_box(
    bib_file,
    text_size: 24pt,
    title: none,
    style: "ieee",
    stretch_to_bottom: false
) --> [content]
```