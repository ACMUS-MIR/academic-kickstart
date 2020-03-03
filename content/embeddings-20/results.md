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


title = "Detailed Results"
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

## 1. Detailed Classification Results:

The following plot shows the classification results for all experiments based on the (best performing) SVM classifier (a). An alternative ordernig can be seen in (b) where results of the same task are neighbored. 

(a)
<img src="/img/embedding/results_diagram_All_Emb.png" alt="Embeddings SVM" border="0px" width="1000"/>

(b)
<img src="/img/embedding/results_diagram_All_Emb_taskwise.png" alt="Embeddings by task SVM" width="1000"/>

Overall averaged results by embedding can be seen in the following figure. One can observe that OpenL3 embeddings outperform all other embeddings as well as the baseline:  

<img src="/img/embedding/avrg_svm_embeddings_results.png" alt="Avrg Embedding SVM" width="600"/>
<br/>

## 2. Tables containing full results
<br/>
Here a detailed view of all classification results for each classifier-task combination can be seen. In table I results are shown when using 80% of the dataset for training followed by 10% of the set for training (table II) to point out the difference of small amounts of data available. Table III shows results early fusion classifiers versus the best late fusion approach. Table IV

<table>
  <tr>
    <td style=" border:0px; background-color:white; padding:13px"><img src="/img/embedding/res_80.png" alt="Avrg Embedding SVM" width="530"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_10.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
  <tr>
	<td style="border:0px;" colspan="2"> I am wondering what is happening when I write some tesxt in here and how it looks like when its bigger than one coloum </td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white; padding-left:40px"><img src="/img/embedding/res_fusion.png" alt="Avrg Embedding SVM" width="500"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_domain.png" alt="Avrg Embedding SVM" width="500"/></br>
	<img src="/img/embedding/res_size.png" alt="Avrg Embedding SVM" width="500"/>
	</td>
  </tr>
</table>





## 3. Confidence Matrices

txt follows or not

<img src="/img/embedding/t1_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t2_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t3_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t4_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t5_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t6_conf_early_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
<img src="/img/embedding/t6_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>


## 4. Baseline models

The following diagram shows the classification results for all experiments ....

<img src="/img/embedding/cnn_flow_han_mod.png" alt="Avrg Embedding SVM" width="500"/>


