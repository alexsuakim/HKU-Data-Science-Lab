# CV-Crayfish-Stress-Level-Detection
This is a computer vision project that classifies videos of crayfish into different stress levels.

## Abstract  
Crayfish display their emotions and mental state with changes in physical behaviour, which can be detected using video clips. Crayfish stress detection is an excellent example of studying the sentience and sentiments of invertebrates since their emotions displayed are simpler than those of other animals. The emotion of crayfish is divided into two main categories: a state of high stress and a normal state with low stress. The stress level of a crayfish can be predicted by tracking its movements that hint at the stress level of a crayfish: body movement, speed, eye movement and the opening and closing of the chelae. 
This project aims to detect the stress level of crayfish by developing a rule-based computer vision model that tracks the physical cues of crayfish. The movement of crayfish is represented numerically by tracking video streams. Results demonstrated an accuracy level of 0.909 after predicting the anxiety level of crayfish into two classes: high and low anxiety. 
By enabling the automation of sentiment detection in invertebrates using machine learning and computer vision, the project aims to assist future studies in marine biology and invertebrate zoology. With further studies on behavioural evidence of invertebrate sentience, updates on the detection model could be further anticipated.

## Introduction 
Crayfish display sentience with different physical behaviours and visual cues. Due to the lack of complexity, invertebrate sentience is simpler to analyse than human sentience. The telencephalon in the invertebrate brain can react similarly to the mammalian amygdala and hippocampus (Kittilsen, 2013). The hippocampus and amygdala are parts of the brain that are closely connected. The hippocampus and prefrontal cortex interpret the threat perceived. They process the context of the perceived fear to determine whether it is accurate. Thus, with telencephalon, invertebrates such as crayfish can also feel stress and anxiety (Murilo, 2019). Different stress levels cause crayfish to show different adaptive behaviours to minimise the threat they are expecting (The Independent, 2014).
The project aims to incorporate machine learning and computer vision techniques to automate the stress level detection of crayfish. The detection model is a rule-based model that determines the stress level of crayfish by representing the movement level of the crayfish numerically. The model mainly considers the movement level since crayfish tend to show less movement when anxious or stressed, as behavioural evidence of fear for the surrounding environment. With further studies on crayfish sentience, the project could be further expanded to classify the crayfish video streams into many more classes and emotions besides the stress level. The project could also be expanded to automatically detect the sentience of more invertebrates or marine animals other than crayfish.
 The crayfish stress detection model could assist future studies in marine biology, such as the sociality levels of marine invertebrates. Like many fish species, crayfish are known to be social animals, meaning they are more likely to feel fear or anxiety in an individual setting than in a group environment. Furthermore, the model could assist in studies on invertebrate zoology. Through automated stress detection, studies could easily find out in what settings crayfish or other invertebrates feel stressed or fearful. 

## Literature Review 
Detecting stress and disease is critical in the industrial development of crayfish. Since stress is one of the main factors hindering crayfish's life, breeding them in a stress-free environment can promote their growth and development. Research on stress- and disease-resistant crayfish genotypes shows that juvenile crayfish with the stress- and disease-resistant genes showed a mortality rate decreased by 20%. The juvenile survival rate is vital in the crayfish population since it leads to sexual maturity and propagation. 
The invertebrate model system of crayfish makes it possible to examine anxiety- and stress-related reactions in less complex nervous systems. Crayfish avoid high-intensity lighting, exposed locations, decreased activity and exploratory behaviours, and increased tremors in their chelae and compound eyes when exposed to factors causing stress (Fossat et al., 2014). 
Crayfish can show anxiety-induced behaviour when confronting different physical and social situations. Crayfish showed more stress behaviours after a painful experience, such as an electric shock (Fossat et al., 2015), meaning that physical pain can induce anxiety even in simple invertebrates such as crayfish. They quickly learned to avoid the places related to pain experience and started to avoid light arms of a dark/light plus maze. Social situations such as social harassment or lowering one's social status could also induce similar stress- or anxiety-related behaviours in crayfish (Bacqué-Cazenave et al., 2017). Crayfish can live isolated or in groups, depending on their environment. When two crayfish isolated in territorial conditions are placed in a restricted space, they fight until one escapes. The winner and the loser crayfish will be displaying different behaviours. The loser typically depicts submissive and anxiety-like behaviour, whereas the winner depicts aggressive behaviours such as harassing the loser. The study shows how social interactions of invertebrates can affect their emotions and cause anxiety-induced behaviours. 
Anxiety-induced behaviour can be observed in crayfish not only when they are physically or socially distressed but also when they are injected with serotonin or other anxiety-inducing substances. Feelings of stress and anxiety display coherent characteristics across different species and even kingdoms. Studies on anxiety-related responses of neurotransmitters show that even mammals such as humans and invertebrates such as crayfish share a common neurological foundation. Stressed crayfish showed higher levels of serotonin compared to the unstressed control group. When the unstressed crayfish were injected with serotonin, however, they started to show signs of stress and displayed a reduction in time moving and exploring the illuminated arms (Fossat, 2014). Other experiments on stimulants also showed crayfish displaying anxious behaviours when injected with anxiety-inducing substances such as caffeine (Bacqué-Cazenave et al., 2017). On the contrary, studies have shown that giving anti-anxiety substances, such as benzodiazepines, to crayfish showing anxiety-induced behaviour can effectively lower their stress levels (Catania, 2013). 
Emotion of crayfish can be detected from different physical and behavioural cues. Different behavioural evidence includes body, eye, and chela movement. More body movement indicates less stress since invertebrates tend to move around and explore the surrounding space more actively when they feel less stressed (Fossat, 2014). When stressed, however, they tend to explore the illuminated parts less and prefer to stay safely in the dark. The same is shown in other invertebrates, such as zebrafish. Anxious zebrafish take more freezing motion, swim slowly and show more irregular motions (Nodulus, 2023).
The anxiety level of invertebrates is affected by various stimuli, and the different stimuli are tested with novel tank tests (NTT) and light-dark tests (LDT) (de Abreu, 2019). LDTs were performed with different light intensities and hues, where crayfish's physical and behavioural movements were monitored. Different light intensities included low, medium and high. Different hues included white, blue, yellow, and red. The environments with different light intensity and hue were to expose the crayfish to different settings to monitor and detect the different stress levels of crayfish. 
Crayfish body movement is one of the most evident signs of crayfish stress levels. The body movement is calculated first by detecting crayfish. Crayfish are detected by training the pre-trained YOLOv8 model. Object detection is a task in computer vision that is used to detect objects in images or videos. It is performed by localising a region within an image and classifying the image within the bounding box for the object of interest. YOLO, short for You Only Look Once, is a single-shot object detection method which combines the two steps of object detection: prediction of bounding boxes and class probabilities. Since many different bounding boxes of different locations and sizes can be classified as accurate for the same object, YOLO uses non-maximum suppression (NMS) to produce a single bounding box for an object, removing all the redundant ones.
            
## Research Method 
This project aims to detect the stress level of crayfish by tracking their movements in videos. The levels of movements of crayfish largely depend on their stress levels. The more stressed the crayfish are, the more likely they will stay inactive, usually in the corner, to seek safety. On the contrary, if the crayfish move around and explore more actively in the tank, they are less stressed.
The data source includes videos of crayfish in tanks with different light intensity and hue, and the behaviours of crayfish were monitored. Crayfish were set in tanks with different light settings to expose them to various surroundings for observing different stress levels. Different light intensities included low, medium and high, and different hues included white, blue, yellow and red. 
In order to detect crayfish effectively in different poses from different angles, crayfish images had to be annotated, augmented and split into different sets. We gathered over 70 images containing crayfish in different light settings, including hue and intensity, and from different angles and poses. The images were annotated with bounding boxes containing the crayfish. The image set was pre-processed by auto-orienting and resizing. The images were augmented through horizontal flipping and applying colour changes such as hue for more accurate detection results. The image set was split into 80% training set, 15% validation and 5% testing set. 
A pre-trained YOLOv8 was used to initialise the parameters for detecting crayfish and was then explicitly trained on crayfish images to work as a custom detector. The model was fed with the training set images and was trained for up to 25 epochs. 
When a crayfish is detected in a video, its location in the tank is recorded every ten frames. For every saved location, the distance between the previous location is calculated. The distances are all added up, and the sum is then divided by the number of frames in the video. The function of the movement is as follows:
                               
Crayfish were considered stressed when their movement value was lower than 7.0 and not stressed otherwise. The crayfish videos from multiple light settings were tested for the accuracy of the classification prediction. 

## Results 
For crayfish detection, the model showed a test set accuracy of a precision of 1.0, a recall of 0.863, and a mAP50 of 0.938 after 25 epochs, where mAP stands for mean average precision.
           
![image](https://github.com/alexsuakim/CV-Crayfish-Stress-Level-Detection/assets/99973140/5510aa57-86d2-4487-944a-87fd5d4d43de)

 
### Figure 1
In Figure 1, the graphs illustrate the model performance for each epoch. The performance metrics, such as training and validation loss and mAP, show how well the model detects crayfish in each epoch. Most metrics showed the best performance at the 21st epoch. The weights for the best model (weights after the 21st epoch) were used for detecting the crayfish.  
  
 ![image](https://github.com/alexsuakim/CV-Crayfish-Stress-Level-Detection/assets/99973140/075198d2-24a7-47de-8f28-5236e6658e31)

### Figure 2
Images from Figure 2 are examples of crayfish detected in different light settings, poses and angles. The bounding boxes are shown on images or videos after the detection with the confidence rounded to the nearest tenth. 
Crayfish tend to show less movement during a specific period when they are stressed compared to how they freely move around when they are not stressed. From an input video, crayfish is detected every ten frames and the coordinates and the size of the bounding boxes are logged. The movement of crayfish is determined by adding up the distance the crayfish moved from one frame to another. The total distance is then divided by the number of frames to get the movement of the crayfish regardless of the number of frames in the video. The movement value is then compared to the cut-off value, which is 7.0, to determine whether it is stressed. If the cut-off value is greater than the movement value, it is more likely that the crayfish is stressed, and if the movement value is greater than the cut-off line, it is more likely that the crayfish is not stressed. 
The movement's mean, median and variance for the norm class were 11.582, 11.291, and 12.737, respectively. On the other hand, the mean, median and variance of the movement for the stressed class were 5.975, 5.131, and 6.665, respectively, rounded to the nearest thousandth. Clearly, the norm class shows much more movement than the stressed class. The accuracy of the available crayfish videos taken in different light settings was 0.909. 

## Discussion 
Crayfish show several physical cues when they are stressed, such as a decrease in body movement and an increase in pupil and chelae movement. A decrease in body movement is the most pronounced evidence of stress, and movement can be detected by locating the crayfish in their tanks. Crayfish could be located with the mAP50 of 0.938 by training a YOLOv8, and their according stress levels could be predicted with the accuracy of 0.909. 
Although detecting crayfish showed high-accuracy results, some shortcomings could still be solved. It is not easy to correctly consider the distance when the crayfish moves back and forth in a tank when the videos are taken from the front. Moreover, since the tanks are mirror-like on the edges, the mirror reflection is sometimes detected as crayfish. This could detect more than one crayfish in one tank when there is only one in reality. After solving these shortcomings, higher accuracy could be expected, while more emotions could be added to the predictor. Since the stress levels of crayfish are a great simple example of invertebrate sentience, this could be an excellent opportunity for more studies related to invertebrate and vertebrate sentience.

## Conclusion
By enabling the automation of stress detection in crayfish, this project aims to provide a tool for future studies in invertebrate sentience and marine biology. The emotion detection model could be further developed with further studies on behavioural signs of different emotions in crayfish and other invertebrates. This could assist in studies on invertebrate emotions and their social interactions, health and breeding. Natural environments other than tanks, such as freshwater lakes, ponds and streams, could also be added for better detection results. 

