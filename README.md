# Visualization-of-CNN-toward-Pneumonia-Detection-in-CXRs

Feel free to use the attached notebooks for your own model and data. Kindly cite the publication as these codes are part of this published work:

### Rajaraman S, Candemir S, Kim I, Thoma GR, Antani SK. Visualization and Interpretation of Convolutional Neural Network Predictions in Detecting Pneumonia in Pediatric Chest Radiographs. Appl. Sci. 2018, 8, 1715

# Prerequisites:

Keras>=2.2.0

Tensorflow-GPU>=1.9.0

OpenCV>=3.3

In this study, we evaluate, visualize, and explain the performance of CNNs to detect pneumonia and further differentiate between bacterial and viral types in pediatric Chest radiographs. We present a novel visualization strategy to localize the region of interest that is considered relevant for model predictions across all the inputs that belong to an expected class. We used a set of pediatric CXRs that have been made publicly available by:

Kermany, D.S.; Goldbaum, M.; Cai, W.; Valentim, C.C.S.; Liang, H.; Baxter, S.L.; McKeown, A.; Yang, G.; Wu, X.; Yan, F.; et al. Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning. Cell 2018, 172, 1122–1131. 

The CXRs contain regions other than the lungs that do not contribute to diagnosing pneumonia. We used an algorithm based on anatomical atlases to automatically detect the lung ROI and cropped them to the size of the bounding box and resampled to 1024 X 1024 pixel dimensions. The source code for the same can be found at https://ceb.nlm.nih.gov/proj/tb/Segmentation_Module_Version_2017_11_04.zip. 
We evaluated the performance of different types of custom CNNs including (i) Sequential CNN; (ii) CNN with residual connections (Residual CNN); (iii) CNN with Inception modules, and (iv) Pretrained VGG16 model in detecting pneumonia and furthermore distinguishing between bacterial and viral types. We evaluated the performance of these CNNs in terms of the following performance metrics: (i) accuracy; (ii) AUC; (iii) precision; (iv) recall; (v) specificity; (vi) F-Score; and, (vii) Matthews Correlation Coefficient (MCC).

# Visualization studies:
The interpretation and understanding of CNNs is a hotly debated topic in ML, particularly in the context of clinical decision-making. CNNs are perceived as black boxes and it is imperative to explain their working to build trust in their predictions. The methods of visualizing CNNs are broadly categorized into (i) preliminary methods that help to visualize the overall structure of the model; and, (ii) gradient-based methods that manipulate the gradients from the forward and backward pass during training. We performed the following visualization studies:

# Visual Explanation through Discriminative Localization: 
We performed class activation maps (CAM) and gradient-weighted CAM visualizations to understand the learned model behavior.  We propose novel visualization methods including average-CAM and average grad-CAM to represent the class-level ROI that is most commonly considered significant for correct prediction across all the inputs that belong to a given class. Further details pertaining to the process can be found in the published paper.  

# Locally Interpretable Model-Agnostic Visual Explanations (LIME):
In the publication entitled “Why Should I Trust You?- Explaining the Predictions of Any Classifier”, the authors explain a framework called LIME (Locally Interpretable Model-Agnostic Explanations), which is an algorithm that can explain the predictions of any classifier in a faithful way by approximating it locally with an interpretable model.  We used this visualization tool to explain the learned behavior of the model toward detecting pneumonia and further differentiate bacterial and viral pneumonia types. The details pertaining to these studies can be found in our published paper.  
