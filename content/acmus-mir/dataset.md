+++
# A Demo section created with the Blank widget.
# Any elements can be added in the body: https://sourcethemes.com/academic/docs/writing-markdown-latex/
# Add more sections by duplicating this file and customizing to your requirements.

widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 15  # Order that this section will appear.
share = false
profile = false
date = "2019-06-23"


title = "ACMUS-MIR DATASET"
subtitle = ""

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "1"

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "white"
  
  # Background gradient.
  #gradient_start = "DarkGreen"
  # gradient_end = "ForestGreen"
  
  # Background image.
  # image = "image.jpg"  # Name of image in `static/img/`.
  # image_darken = 0.6  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.

  # Text color (true=light or false=dark).
  # text_color_light = true

[design.spacing]
  # Customize the section spacing. Order is top, right, bottom, left.
  padding = ["20px", "0", "20px", "0"]

[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""

+++

![Andes region of Colombia](/img/andes.png#floatright)
The ACMUS-MIR datas set is a growing collection of annotated music from the [Andes region of Colombia]({{< ref "/andes-music/index.md" >}}). 
The data set was compiled with the goal of supporting the different MIR task addressed in our project: [meter extraction]({{< ref "/project/meterextraction.md" >}}), 
[instrumental format recognition]({{< ref "/project/ensemblesize.md" >}}), [speech/music discrimination]({{< ref "/project/speechmusic.md" >}}) , and [scale detection in music]({{< ref "/project/scale.md" >}}).
For each of these tasks, a dedicated collection of music was compiled and annotated by musicologist in Colombia. 

The ACMUS-MIR data set has been made publicly available for the wider research community as a Zenodo repository[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3965447.svg)](https://doi.org/10.5281/zenodo.3965447)
<br>

For a detailed description of the dataset, please refer to our DLfM 2019 [publication.](https://dlsi.ua.es/gent/drizo/dlfm2019/mora.pdf) For information about the different versions of the ACMUS-MIR dataset, see the links below:
- [v1.0]({{< ref "/acmus-log/v10.md" >}})
- [v1.1]({{< ref "/acmus-log/v11.md" >}})






## Rhtyhm Set
Bambuco - 6/8 <br>
{{< audio src="rh_0001.wav" >}}


Bambuco - 6/8 <br>
{{< audio src="rh_0002.wav" >}}


Bambuco - 6/8 <br>
{{< audio src="rh_0003.wav" >}}


Guabina - 3/4 <br>
{{< audio src="rh_0004.wav" >}}


 Pasillo - 3/4 <br>
 {{< audio src="rh_0005.wav" >}}



## Instrumental Format Set 
Solo tiple  <br>
{{< audio src="if_0112.wav" >}}


Solo bandola  <br>
{{< audio src="if_0134.wav" >}}


Solo guitar  <br>
{{< audio src="if_0015.wav" >}}


Duet - tiple, guitar <br>
{{< audio src="if_0056.wav" >}}


Trio - bandola, tiple, guitar <br>
{{< audio src="if_0162.wav" >}}


Quartet -  2 bandolas, tiple, guitar<br>
{{< audio src="if_0167.wav" >}}


Quintet - 2 bandolas, tiple, guitar, bass <br>
{{< audio src="if_0103.wav" >}}


Large ensemble <br>
{{< audio src="if_0113.wav" >}}


## Scale Set
Ab - Major - 4 instruments <br>
{{< audio src="sc_0001.wav" >}}

Eb - Minor - 4 instruments <br>
{{< audio src="sc_0002.wav" >}}


F - Major - 4 instruments <br>
{{< audio src="sc_0003.wav" >}}


Bb - Major - 4 instruments <br>
{{< audio src="sc_0004.wav" >}}


Eb - Minor - 4 instruments <br>
{{< audio src="sc_0005.wav" >}}





