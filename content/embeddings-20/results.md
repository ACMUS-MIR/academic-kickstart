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

The following plot shows the classification results for all experiments based on the (best performing) lineaar SVM classifier (a). An alternative ordernig can be seen in (b) where results of the same task are neighbored. 

(a)
<img src="/img/embedding/results_diagram_All_Emb.png" alt="Embeddings SVM" border="0px" width="1000"/>

(b)
<img src="/img/embedding/results_diagram_All_Emb_taskwise.png" alt="Embeddings by task SVM" width="1000"/>

Overall averaged results for each embedding using linear SVM can be seen in the following figure. One can observe that OpenL3 embeddings outperform all other embeddings and performs nearly similar to the baseline:  

<img src="/img/embedding/avrg_svm_embeddings_results.png" alt="Avrg Embedding SVM" width="600"/>
<br/>

## 2. Tables containing detailed results
<br/>
The following tables contain detailed results for each classifier-task combination can be seen. Table I shows results when using 80% of the dataset for training. Table II displays the results using only 10% of the set for training to point out the difference between embeddings and baseline for small datasets. Here OpenL3 combined with a linear SVM outperforms the other embeddings as well as the baseline. 

<table>
  <tr>
    <td style=" border:0px; background-color:white; padding:13px"><img src="/img/embedding/res_80.png" alt="Avrg Embedding SVM" width="530"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_10.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
  <tr>
	<td style="border:0px;" colspan="2"> Table III shows results of early fusion versus late fusion approach. Despite of task 6 late fusion is performing best on all experiments. The comparison of different OpenL3 embeddings are placed in table IV. Environmental embeddings perform constantly worse compared to the one trained on the music domain. Table V illustrates the results of standard size OpenL3 embeddings with 512 values and larger embeddings consisting of 6144 values. Apart from task 1 large size embeddings perform slightly better but are also expensive in terms of computational costs. Also the best combination between between size and classifier varies making 512 output values and linear SVM classifier the best combination on average.</td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white; padding-left:10px"><img src="/img/embedding/res_fusion.png" alt="Avrg Embedding SVM" width="530"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_domain.png" alt="Avrg Embedding SVM" width="500"/></br>
	<img src="/img/embedding/res_size.png" alt="Avrg Embedding SVM" width="500"/>
	</td>
  </tr>
</table>

## 3. Confidence Matrices

In this section the confusion matrices of all tasks are displayed. Each matrix shows mean filewise accuracy of the corresponding classification task. 

<table>
  <tr>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t1_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 1 - Ensemble Size Classification in Music</td>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t2_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 2 -  Musical  Instrument  Family  Recognition</td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t3_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 3 - Speech Music Classification</td>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t4_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 4 - Classification  of  Operational  States  in  Electric   Engines</td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t5_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 5 - Metal  Surface  Classification</td>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t6_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 6 - Plastic  Material  Classification</td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t6_conf_early_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 6 - Plastic  Material  Classification (Early Fusion)</td>
    <td style=" border:0px; background-color:white"><img src="/img/embedding/t6_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br>
	Task 6 - Plastic  Material  Classification (Late Fusion)</td>
  </tr>
</table>


## 4. Baseline models

Here the baseline model of task 2 (Musical  Instrument  Family  Recognition) can be seen. 

The first plot shows the actual model used for this publication. In contrast to the original model (below) each convolutional block has only half of the layers (two  of  the  original  four  convolutional  blocks have been removed) and after each block batch normalization is applied. Dropout has been moved to the end of the model to avoid overfitting. Finally, the Sigmoid activation has been replaced with a softmax activation in the output layer since the application is a single label task. 

<img src="/img/embedding/cnn_flow_han_mod.png" alt="Avrg Embedding SVM" width="600"/>

The second plot describes the original model from Han et. al (Y. Han, J. Kim, and K. Lee, “Deep Convolutional Neural Networks forPredominant Instrument Recognition in Polyphonic Music,”IEEE/ACMTransactions on Audio, Speech, and Language Processing, vol. PP, 2016.). 

<img src="/img/embedding/cnn_flow_han_orig.png" alt="Avrg Embedding SVM" width="600"/>

The following image shows the baseline model used for the task1 and task 3. It is a CNN with 4 convolutional layers with a 3x3 kernel and a fully connected (dense) layer at the end. Max Pooling and dropout is applied after each block and a softmax activation is used for the output layer. The number of filters doubles in each conv. block and starts with 16.

<img src="/img/embedding/cnn_flow_nice.png" alt="Avrg Embedding SVM" width="600"/>


