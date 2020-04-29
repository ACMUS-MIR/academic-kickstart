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


title = "Analyzing the potential of pre-trained embeddings for audio classification tasks"
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

## 1. Detailed classification results <a name="detailed"></a>

The following plot (a) shows the classification results for all experiments based on the (best performing) linear SVM classifier. An alternative ordernig can be seen in (b) where results of the same task are grouped together. 

(a)

<img src="/img/embedding/results_diagram_All_Emb.png" alt="Embeddings SVM" border="0px" width="900"/>

(b)
<img src="/img/embedding/results_diagram_All_Emb_taskwise.png" alt="Embeddings by task SVM" width="900"/>

Overall average results for each embedding using linear SVM can be seen in the following figure. One can observe that OpenL3 embeddings outperform all other embeddings, and obtain comparable  results to the baseline model:  

<img src="/img/embedding/avrg_svm_embeddings_results.png" alt="Avrg Embedding SVM" width="600"/>
<br/>

## 2. Tables containing detailed results <a name="tables"></a>
<br/>
The following tables contain detailed results for each classifier-task combination. Table I shows results when using 80% of the dataset for training. To highlight the difference between embeddings and baseline models for small datasets, Table II displays the results using only 10% of the set for training. Here OpenL3 combined with a linear SVM outperforms the other embeddings as well as the baseline. 

<table>
  <tr>
    <td style=" border:0px; background-color:white; padding:7px"><img src="/img/embedding/res_80.png" alt="Avrg Embedding SVM" width="500"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_10.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
  <tr>
	<td style="border:0px;" colspan="2"> Table III shows results comparing early fusion with late fusion approaches. Apart from task 6, late fusion performs best in all experiments. Table IV presents a comparison between different OpenL3 embeddings. Environmental embeddings perform constantly worse compared to the ones trained on  music. Table V illustrates the results with OpenL3 embeddings with 512 values and larger embeddings with of 6144 values. Apart from Task 1, all tasks show better results with larger embeddings. However, larger embeddings are more computationally expensive.</td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white; padding-left:10px"><img src="/img/embedding/res_fusion.png" alt="Avrg Embedding SVM" width="530"/></td>
	<td style=" border:0px; background-color:white"><img src="/img/embedding/res_domain.png" alt="Avrg Embedding SVM" width="500"/></br>
	<img src="/img/embedding/res_size.png" alt="Avrg Embedding SVM" width="500"/>
	</td>
  </tr>
</table>

## 3. Confusion matrices <a name="matrices"></a>

In this section, the confusion matrices with mean file-wise accuracy for all tasks are shown. 

<table>
  <tr>
    <td style=" border:0px; background-color:white">Task 1 - Ensemble Size Classification in Music</br><img src="/img/embedding/t1_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
    <td style=" border:0px; background-color:white">Task 2 -  Musical  Instrument  Family  Recognition</br><img src="/img/embedding/t2_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white">Task 3 - Speech Music Classification</br><img src="/img/embedding/t3_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/>
	</td>
    <td style=" border:0px; background-color:white">Task 4 - Classification  of  Operational  States  in  Electric   Engines</br><img src="/img/embedding/t4_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></br></td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white">Task 5 - Metal  Surface  Classification</br><img src="/img/embedding/t5_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
    <td style=" border:0px; background-color:white">Task 6 - Plastic  Material  Classification</br><img src="/img/embedding/t6_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
  <tr>
    <td style=" border:0px; background-color:white">	Task 6 - Plastic  Material  Classification (Early Fusion)</br><img src="/img/embedding/t6_conf_early_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
    <td style=" border:0px; background-color:white">Task 6 - Plastic  Material  Classification (Late Fusion)</br><img src="/img/embedding/t6_conf_late_o3_svm.png" alt="Avrg Embedding SVM" width="500"/></td>
  </tr>
</table>


## 4. Baseline models <a name="baseline"></a>

Here the baseline model of task 2 (Musical  Instrument  Family  Recognition) can be seen. 

The first plot shows the actual model used for this publication. In contrast to the original model (below), each convolutional block has only half of the layers (two  of  the  original  four  convolutional  blocks have been removed). After each block, batch normalization is applied. Dropout has been moved to the end of the model to avoid overfitting. Finally, the Sigmoid activation has been replaced with a softmax activation in the output layer since the application is a single label task. 

<img src="/img/embedding/cnn_flow_han_mod.png" alt="Avrg Embedding SVM" width="600"/>

The  plot below describes the original model from Han et. al [Y. Han, J. Kim, and K. Lee, “Deep Convolutional Neural Networks for Predominant Instrument Recognition in Polyphonic Music,”IEEE/ACMTransactions on Audio, Speech, and Language Processing, vol. PP, 2016.](https://arxiv.org/pdf/1605.09507) 

<img src="/img/embedding/cnn_flow_han_orig.png" alt="Avrg Embedding SVM" width="600"/>

The following image shows the baseline model used for the Task 1 and Task 3. It is a CNN with 4 convolutional layers with a 3x3 kernel and a fully connected (dense) layer at the end. Max Pooling and dropout is applied after each block and a softmax activation is used for the output layer. The number of filters doubles in each convolutional block and starts with 16.

<img src="/img/embedding/cnn_flow_nice.png" alt="Avrg Embedding SVM" width="600"/>


