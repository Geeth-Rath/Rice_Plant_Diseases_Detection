**Detecting and classifying nutrient deficiencies**

Module 3 is dedicated to addressing the detection and classification of nutrient deficiencies in paddy leaves. One of the challenges in this task is distinguishing between primary nutrient deficiencies such as Nitrogen, Phosphorus, and Potassium, which often exhibit similar symptoms. To overcome this challenge, Module 3 focuses on identifying the distinct characteristics of each nutrient deficiency, enabling accurate differentiation.

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.001.png)

*Figure 30: Classification classes*

**Identification of N, K, and P Deficiencies in the Paddy Leaves**

Visible symptoms associated with nutrient deficiencies in nitrogen (N), potassium (K), and phosphorus (P) are often observed in the upper level of paddy leaves. These symptoms include changes in leaf color and alterations in leaf morphology. Insufficient chlorophyll production is indicated by a pale green or yellowish leaf color, characteristic of nitrogen deficiency. Leaf withering, characterized by yellow or brown discoloration at the leaf tips and edges, is a common symptom of potassium deficiency. Phosphorus deficiency typically manifests as dark green or yellowish discoloration.

- N Deficiency:

In the case of an N deficiency, a higher concentration of yellow color compared to green color is generally observed in the paddy leaf. This observation suggests reduced chlorophyll content due to insufficient nitrogen levels, which directly affects the photosynthetic capacity of the plant.

- P Deficiency:

When analysing a paddy leaf image with a P deficiency, a prominent yellowish-brown coloration is typically observed in the upper part of the leaf, indicating a lack of phosphorus. Conversely, the lower part exhibits a higher proportion of greenish color, as an adequate supply of phosphorus is available for chlorophyll synthesis in the lower levels of the leaf.

- K Deficiency:

In the case of a K deficiency, the leaf may demonstrate similar greenish color, albeit with a slight presence of yellow. However, the overall greenish color remains higher than the yellow color . This color distribution signifies insufficient Potassium levels required for chlorophyll production, resulting in slight leaf yellowing.

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.002.png)

*Figure 32: Macro deficiencies of padday leaves. (Phosperrous, Nitrogen and Pottasium defficencies)*

The datasets retrieved by Kaggle and Mendeley sites were utilized during the testing and implementation  stages.  Kaggle  dataset  includes  images  for  NPK  deficiencies  while Mendeley has a dataset only for N deficiencies.  Kaggle contains 125, 111 and 183 numbers of images for P, N, and K deficiencies respectively.

**Identification of Color Ranges for Each Disease**

The  determination  of  specific  color  ranges  for  different  diseases  necessitates  a comprehensive dataset of paddy leaf images with known diseases. Advanced image processing techniques, statistical analysis are employed to establish characteristic color ranges associated with each disease. This step serves as the foundation for accurate disease identification and differentiation.

- **Consideration of the Yellow to Green Color Range:**

Within the analysis of paddy leaves, particular attention is given to the color range spanning from yellow to green, as it captures variations associated with nutrient deficiencies and diseases. Focusing on this color range enables the identification and differentiation of abnormal color patterns indicative of underlying issues affecting plant health.

- **Utilizing Color Analysis and the HSV Color Model:**

Color analysis techniques are employed to extract valuable information from paddy leaf images. The HSV (Hue, Saturation, Value) color model is particularly well-suited for this purpose as it allows for the separation of color components based on human perception. The HSV model comprises three components: Hue, Saturation, and Value. Hue represents the color itself, Saturation determines the intensity or purity of the color, and Value represents the brightness or darkness.

- **Image Positioning** 

The image was positioned at the center of a blank canvas or background image. The decision to place the image at the center was made based on the assumption that the selected leaves used for analysis possess a symmetrical structure. By aligning the paddy leaf in the center of the image, it becomes easier to perform subsequent analysis and measurements on the leaf's features, as the symmetrical nature of the leaf allows for consistent and accurate assessments. This centered placement of the image not only facilitates the analysis process but also aids in comparing different leaves and identifying patterns or irregularities in their structures.

- **Technique of splitting paddy leaf**

The technique of splitting paddy leaf images into two halves facilitates a detailed analysis of color distribution. This approach allows for a comparative examination of color patterns within the leaf, providing insights into potential variations between upper and lower parts of the same leaf. Leaf should be horizontally symmetrical so that comparing  the  halves  enables  the  identification  of  distinct  color  characteristics associated with specific nutrient deficiencies or diseases.  According to the diagram, splitting concept can be utilized  to analyse the colour patterns of the deficiencies.

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.003.png)

*Figure 33:Upper and lower half of the paddy leaf (include K, N, P deficiencies respectively)*

*Figure 34: Original image(P deficiency ) and Back ground removed Splitted image![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.004.png)![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.005.png)*

**5.2.2.3.3 Color Analysis**

The analysis of leaf color is a crucial factor in detecting nutrient deficiencies in paddy plants. Analysis methodology utilizes the green and yellow pixel counts in lower and upper parts of paddy leaves. By employing the HSV color model, specific color ranges are established for  Nitrogen  (N), Phosphorus  (P),  and  Potassium  (K)  deficiencies. The methodology involves calculating the percentages of green and yellow pixels and comparing them  against  predefined  color  ranges  to  accurately  identify  the  respective  nutrient deficiencies.

**Color Ranges for Nitrogen (N) Deficiency:**

The analysis of color in the HSV (Hue, Saturation, Value) color model provides valuable insights into identifying nutrient deficiencies in paddy leaves. Here's how to interpret the HSV color model perspective for the given color ranges. Green and Yellow color pixels  can be separately identify for N defficeincy is identified as below.

- Green Color Range:

The green color range is defined by the following values:

- Lower Limit: Hue = 50, Saturation = 40, Value = 40
- Upper Limit: Hue = 138, Saturation = 255, Value = 255

The Hue component represents the actual color, with values ranging from 50 to 138. Saturation determines the intensity or purity of the color, ranging from 40 to 255, where higher values indicate more vibrant and intense shades of green. The Value component represents the brightness or lightness, ranging from 40 to 255, with higher values indicating brighter shades of green.

- Yellow Color Range:

The yellow color range is defined by the following values:

- Lower Limit: Hue = 20, Saturation = 40, Value = 40
- Upper Limit: Hue = 50, Saturation = 255, Value = 255

Similarly, the Hue component ranges from 20 to 50, representing the hues associated with yellow. Saturation values ranging from 40 to 255 indicate different levels of intensity, with higher values representing more vibrant shades of yellow. The Value component ranges from 40 to 255, representing the brightness levels, where higher values correspond to brighter shades of yellow.

**Color Ranges for Phosphorus (P) and Potassium (K):**

In the analysis of nutrient deficiencies in paddy leaves using the HSV color model, the following color ranges are considered for identifying Phosphorus (P) and Potassium (K) deficiencies.

- Green Color Range:

The green color range, defined by the values below, helps identify deficiencies related to phosphorus (P) and potassium (K):

- Lower Limit: Hue = 36, Saturation = 65, Value = 125
- Upper Limit: Hue = 138, Saturation = 255, Value = 255

In this range, the Hue component spans from 36 to 138, indicating the hues associated with various shades of green. The Saturation component ranges from 65 to 255, representing the intensity or purity of the green color. Higher saturation values indicate more vibrant shades of green. The Value component, ranging from 125 to 255, represents the brightness or lightness of the green color. Higher values signify brighter shades of green.

- Yellow Color Range:

The yellow color range, which is considered for phosphorus (P) and potassium (K) deficiencies, is defined as follows:

oLower Limit: Hue = 0, Saturation = 0, Value = 20

oUpper Limit: Hue = 29, Saturation = 255, Value = 255

In this range, the Hue component ranges from 0 to 29, encompassing the hues associated with different shades of yellow. The Saturation component ranges from 0 to 255, representing the intensity or purity of the yellow color. Higher saturation values indicate more vibrant shades of yellow. The Value component, ranging from 20 to 255, represents the brightness or lightness of the yellow color. Higher values indicate brighter shades of yellow.

**Calculation of Pixel Ratio**

When consider pixel ration for upper and lower halves of the leaf, pixel color ratio for each green and yellow color can be calculated as follows.

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.006.png)

*Equation 5: Pixel ratio Calculation*

GRx = Green pixel ratio for the x th  of the leaf YRx = Yellow pixel ratio for the x th part of the leaf NG = number of Green pixel 

NY = number of Yellow pixel 

x  = upper (1) or lower(2) part of the leaf

i = initial pixel

n = nth pixel

- Green pixel ratio for the xth part  of the leaf

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.007.png)

`  `*Equation 6:  Symbolic representation of Green pixel ratio for the xth  of the leaf*

- Yellow pixel ratio for the x th part of the leaf

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.008.png)

*Equation 7: Symbolic representation of Yellow pixel ratio for the x th part of the leaf*

4. **Pixel ratios of  Colour Ranges Nitrogen (N) Deficiency**

Pixel ratios for the upper and lower part of the leaf based on the HSV color range identified for Nitrogen deficiency is illustrated in following fluctuation graphs.

*F i g u![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.009.jpeg)*

*re 35: Pixel ratio fluctuation graph for Nitrogen:*

*Figure 36: Pixel ratio fluctuation graph for Phosphorus![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.010.jpeg)*

*Figure 37: Pixel ratio fluctuation graph for Pottasium![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.011.jpeg)*

According to above graphs we can clearly identify 97-99% of  yellow prixel ratio and  2- 0.99 % of green pixels ratio for upper and lower part of the Nitrogen Deficiency leaf lay in between above mentioned HSV color ranges. But Pixel ratios for Potassium and Phosphorus deficiencies does not lay on that color range.

5. **Pixel ratios in Color Ranges for Phosphorus (P) and Potassium (K):**

Pixel ratios for upper and lower part of the leaf based on the HSV color range identified for Phosphours and Pottassium deficiencies are  illustrated in following fluctuation graphs.

*Figure 38: Pixel ratio fluctuation graph for Nitrogen![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.012.png)*

*Figure 39: Pixel ratio fluctuation graph for Phosperous![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.013.jpeg)*

*Figure 40: Pixel ratio fluctuation graph for Potassium![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.014.jpeg)*

According to above graphs we can clearly identify around 75-95% of green pixel ratio for upper and lower part of the Potassium Deficiency leaf lay in between above mentioned HSV color ranges. Also, Yellow pixel ration for lower and upper halves of the leaf are 0.99-25 %, 30-45 % respectively. 1-50% , 1-30%, 50-97%, 70-98% pixel ratios can be identified in upper and lower halves of yellow and green pixel ratios  of Phosperous deficient leaves.  But Pixel ratios for Nitrogen deficiencies shows irregular relationship around that color range.

Nutrient deficiencies in paddy plants are determined based on the calculated ratios of yellow and green pixels. The conditions of pixel ratios and their corresponding nutrient deficiencies are identified as follows,

- Nitrogen Deficiency

If the yellow pixel ratio for the upper part of the leaf (yellow\_ratio\_first) is greater than 90% and  the  green  pixel  ratio  for  both  upper  and  lower  parts  (green\_ratio\_first  and green\_ratio\_second) is less than 1%, it indicates a nitrogen deficiency in the plant. The decision is determined based on the HSV color ranges identified for Nitrogen deficiency.

- Potassium Deficiency:

If the yellow pixel ratio for the upper part of the leaf (yellow\_ratio\_first) is greater than 35%, the green pixel ratio for the upper part (green\_ratio\_first) is less than 65%, the yellow pixel ratio for the lower part of the leaf (yellow\_ratio\_second) is greater than 30%, and the green pixel ratio for the lower part (green\_ratio\_second) is less than 75%, it suggests a potassium deficiency.The decision is determined based on the HSV color ranges identified for Potassium deficiency.

- Phosphorus Deficiency:

If the yellow pixel ratio for the upper part of the leaf (yellow\_ratio\_first) is greater than 50%, the green pixel ratio for the upper part (green\_ratio\_first) is less than 55%, the yellow pixel ratio for the lower part of the leaf (yellow\_ratio\_second) is greater than 30%, and the green pixel ratio for the lower part (green\_ratio\_second) is less than 70%, it indicates a phosphorus deficiency.The decision is determined based on the HSV color ranges identified for Phosphorus deficiency.

These conditions are designed to classify the nutrient deficiencies by comparing the proportions of yellow and green pixels in the upper and lower parts of the paddy leaf. By analyzing these ratios, it becomes possible to make inferences about the specific nutrient deficiencies affecting the plant.

![](Aspose.Words.50e9e497-462d-4d4e-9682-dbcac6ac1ffb.015.png)

*Figure 41: Flow diagram of Nutrient classification modle*

This flow diagram represents the sequence of steps for identifying nutrient deficiencies in the order of nitrogen (N), phosphorus (P), and potassium (K) using the calculated green and yellow percentages.

The process begins with calculating the green and yellow pixel counts and then determining their respective percentages. The flow then checks if a nitrogen deficiency is present based on the green and yellow pixel percentages. If a nitrogen deficiency is detected, the process ends at the "End - Nitrogen Deficiency" stage.

If a nitrogen deficiency is not detected, the flow proceeds to check for a phosphorus deficiency. If the green and yellow percentages indicate a phosphorus deficiency, the process ends at the "End - Phosphorus Deficiency" stage.

If neither nitrogen nor phosphorus deficiency is identified, the flow continues to check for a potassium deficiency. If the green and yellow percentages indicate a potassium deficiency, the process ends at the "End - Potassium Deficiency" stage.

By considering these detailed aspects of leaf color analysis, image processing, and color range identification, a robust methodology can be designed to accurately diagnose nutrient deficiencies and differentiate diseases in paddy plants. The integration of color analysis, the HSV color model, and the image splitting technique empowers farmers and researchers to make informed decisions regarding plant health management 
