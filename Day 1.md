## Supervised Learning 

How does Tamil Nadu weatherman predict better than IMD?  
- He does not use a single model, he compares many  
- IMD mostly relies on WRF, GFS, IMD’s own numerical models  
- Tamil Nadu Weatherman manually compares ECMWF, GFS, radar data, wind anomalies  
- He blends all these, multi-model consensus, which reduces error.  
- IMD issues updates every 3 hours, sometimes every 6 hours  
- Tamil Nadu Weatherman uses RADAR and satellite loops minute-by-minute that tracks storm movement, predicts which area will get rain next 1–2 hours  
- Updates based on storm behavior

## 10 practical use cases of supervised learning across each modality -   
## Image
1. Face Recognition (Apple FaceID)
Business Impact: Provides security and fast authentication  
Model Used: CNNs + Siamese Networks + Face Embedding Models  
How Data is Fed: Raw camera image → resized → normalized → fed as pixel    
How Training Works: Millions of face images labeled with identities are used  

2. Medical Imaging Diagnosis (Tumor)  
Business Impact: Reduces radiologist workload, increases diagnostic accuracy  
Model Used: ResNet/DenseNet for classification, U-Net for segmentation.  
Data Input: DICOM or PNG medical scans → converted to grayscale/RGB → standardized → fed into CNN.   
Training: Radiologists provide labeled data (tumor present / absent or pixel masks). Model trained using binary cross-entropy or Dice loss for segmentation.   

3. Autonomous Driving Object Detection (Tesla Autopilot)  
Business Impact: Critical for vehicle safety. Enables lane keeping, collision prevention, pedestrian detection, and navigation.  
Model: YOLOv8, Faster R-CNN, SSD.  
Data Feed: Front camera frame at 30–60 FPS → resized → batched → tensor.  
Training: Millions of annotated images with bounding boxes for cars, pedestrians, lights, etc.  

4. Automated Product Categorization (E-commerce - Amazon)  
Business Impact: Millions of items per day can be uploaded automatically. Reduces human cataloging time, improves search and recommendation, increases sales conversions.  
Model: CNN classifiers (EfficientNet, MobileNet).  
Data Feed:Product images → resized → normalized.  
Training: Labeled images with class tags such as Men’s Shoes → Running → Nike.  

5. OCR (Extracting Text from Images) - Google Lens  
Business Impact: Automates data entry, helps banks process cheques, supports document digitization, improves business efficiency.     
Model: CRNN (CNN + RNN) for text recognition.  
Data Input: Scanned document → text regions extracted → fed as image to OCR.  
Training:Paired datasets (image → text string). Loss: CTC loss (Connectionist Temporal Classification).  

6. Manufacturing Defect Detection - chip quality  
Business Impact:Reduces defective units, prevents costly recalls, ensures product quality    
Model:CNN classifiers, segmentation networks (Mask R-CNN).    
Data Feed:High-resolution product images from assembly line cameras.  
Training:Human inspectors label images as “OK / Defective” or provide defect mask.  

7. Number Plate Recognition - Fastag  
Business Impact:Automates toll collection, enforces traffic laws, reduces manpower, speeds up monitoring.  
Model:YOLO for plate detection + OCR for character reading.  
Data Feed:Traffic camera frames → cropped plates → OCR.  
Training:Bounding boxes + labeled plate text.  

8. Content Moderation (Removing violent content)  
Business Impact: Protects brand from harmful content, ensures safe environment  
Model: CNN Image Classifiers (ResNet, EfficientNet).  
Data Input: Uploaded image → converted to tensor → classified as safe/unsafe.    
Training: Large labeled dataset with categories like “violence”,“safe”.  

9. Visual Search (Pinterest visual search)  
Business Impact: Users instantly find similar products → increases conversion rates in shopping apps.  
Model:Siamese Networks for similarity embedding.  
Data Feed:Query image → embedding vector → nearest-neighbor search.  
Training: Pairs/triplets of similar and dissimilar products.  

10. Satellite Image Land Cover Classification (ISRO)  
Business Impact:Used for agriculture planning, disaster mapping, crop yield prediction, environmental monitoring.  
Model:U-Net, SegNet.   
Data Feed:Satellite multispectral images.  
Training:Pixel-level segmentation labels (water, forest, urban, etc.).

## Text
1. Gmail Spam Filter  
Business Impact: Protects users from spam and phishing attacks.  
Model Used: Naive Bayes, Logistic Regression, BERT.  
Data Input: Email text → tokenized → converted to embeddings.  
Training: Emails labeled as “spam” or “not spam”.  

2.  Autocorrect  
Business Impact: Speeds up typing and reduces effort.  
Model Used: LSTM, Transformer language models.  
Data Input: Typed text → tokenized.  
Training: Large text datasets labeled with next-word sequences.  
  
3. WhatsApp Smart Replies  
Business Impact: Makes chatting faster and more convenient.  
Model Used: Intent + response classification models.   
Data Input: Message text → converted into tokens.  
Training: Sentences labeled with appropriate short replies.  

4. Amazon Review Sentiment Detection  
Business Impact: Helps users judge product quality quickly.  
Model Used: BERT sentiment classifier.  
Data Input: Review text → tokenized → embeddings.  
Training: Reviews labeled as “positive”, “negative”, “neutral”.  
  
5. YouTube Comment Moderation  
Business Impact: Protects community by blocking hate speech and harm.   
Model Used: Transformer toxicity classifier.  
Data Input: Comment text → tensor embeddings.  
Training: Comments labeled as “toxic”, “hate”, “safe”.  

6. Netflix Genre Classification  
Business Impact: Helps users discover content they like.  
Model Used: Text classification models.  
Data Input: Movie/series description text.  
Training: Summaries labeled with genres (Drama, Action, Sci-Fi).  

7. LinkedIn Skill Extraction  
Business Impact: Improves job recommendations and profile matching.  
Model Used: NER models (BERT-CRF).  
Data Input: Resume/profile text.  
Training: Words labeled as skills, roles, qualifications.  

8. Chatbot Intent Recognition  
Business Impact: Automates customer support, reduces call center load.   
Model Used: CNN/LSTM/BERT classifiers.  
Data Input: User query text.  
Training: Sentences labeled with intents (Order Status, Refund, Cancel).  

9. Google Search Query Understanding  
Business Impact: Improves relevance and accuracy of search results.  
Model Used: Transformer-based query classifier.  
Data Input: Query text.  
Training: Queries labeled as “navigational”, “local search”, “shopping”.  

10. Auto-Tagging Notes (Notion, Evernote)  
Business Impact: Helps users quickly organize notes.  
Model Used: Text classification models.  
Data Input: Note text → tokenized.  
Training: Notes labeled with categories (Work, Personal, Tasks).  

## Video
1. CCTV Person Detection (Home Security Cameras)  
Business Impact: Alerts homeowners when a person is detected.  
Model Used: YOLO, Faster R-CNN.  
How Data is Fed: Video → broken into frames → fed as images.  
How Training Works: Frames labeled with bounding boxes.  

2. Zoom Background Blur  
Business Impact: Keeps surroundings private and looks professional.  
Model Used: Semantic segmentation models (U-Net).  
How Data is Fed: Video frame → pixel tensor.  
How Training Works: Frames labeled with foreground / background masks.  

3. Instagram Reels / TikTok Content Moderation  
Business Impact: Removes violent or harmful video content.  
Model Used: Video classifiers (3D CNN, TimeSformer).  
How Data is Fed: Video → sequence of frames.   
How Training Works: Clips labeled as safe vs unsafe. 

4. Driver Drowsiness Detection (Cars)  
Business Impact: Prevents accidents by alerting sleepy drivers.  
Model Used: Eye/face detection CNNs.  
How Data is Fed: Cabin camera video.  
How Training Works: Video labeled as drowsy or alert.  

5. Fitness Apps Form Correction (Home Workouts)  
Business Impact: Helps users exercise correctly at home.  
Model Used: Pose estimation networks (OpenPose).  
How Data is Fed: Video → human keypoints extracted.  
How Training Works: Labeled poses (correct/incorrect form).  

6. Gesture-Based TV or Device Control   
Business Impact: Enables touchless control of TVs, speakers.  
Model Used: 3D CNN gesture classifiers.  
How Data is Fed: Hand movement video.  
How Training Works: Labeled gestures like swipe left/right.  

7. YouTube Video Thumbnail Analysis  
Business Impact: Improves recommendations and click-through rates.  
Model Used: Thumbnail image classifier + object detectors.  
How Data is Fed: Key video frames.  
How Training Works: Frames labeled with content attributes.  

8. Doorbell Camera Package Detection  
Business Impact: Alerts when a package is dropped off.  
Model Used: Object detection (YOLO).  
How Data is Fed: Doorbell camera video.  
How Training Works: Labeled bounding boxes around packages.  

9. Video Stabilization (Phone Cameras)  
Business Impact: Produces smoother videos.  
Model Used: Motion estimation models.  
How Data is Fed: Consecutive frames.  
How Training Works: Labeled examples of shaky vs stable frames.  
  
10. Video Face Recognition (Airports, Offices)  
Business Impact: Enables automated security checks and attendance.  
Model Used: CNN face recognition + tracking models.  
How Data is Fed: Face crops from video frames.  
How Training Works: Labeled identities across sequences.  

## Tabular Structure
1. Credit Card Fraud Detection  
Business Impact: Prevents financial losses and protects customers.  
Model Used: XGBoost, Random Forest.  
How Data is Fed: Transaction rows (amount, location, time).  
How Training Works: Transactions labeled fraud or legit.  

2. Loan Eligibility Prediction  
Business Impact: Speeds up loan approvals for banks.   
Model Used: Logistic Regression, Decision Trees. 
How Data is Fed: Customer income, credit score, debt.  
How Training Works: Historical loan data labeled approved/rejected.  

3. Liking Prediction (Telecom, Netflix)  
Business Impact: Helps retain customers before they cancel.  
Model Used: Gradient Boosting, Logistic Regression.  
How Data is Fed: Customer usage patterns.  
How Training Works: Labeled liked or not liked   

4. Salary Prediction (HR Analytics)  
Business Impact: Helps companies benchmark salaries.   
Model Used: Linear Regression.   
How Data is Fed: Experience, skills, location. 
How Training Works: Rows labeled with actual salary.  

5. Sales Forecasting (Retail)  
Business Impact: Optimizes inventory and reduces losses.  
Model Used: Gradient Boosting Regressors.  
How Data is Fed: Daily/monthly sales records.  
How Training Works: Labeled with next-day/month sales numbers.  

6. Insurance Claim Prediction  
Business Impact: Prevents fraud and speeds up claims processing.  
Model Used: Random Forest.  
How Data is Fed: Policyholder data in rows.  
How Training Works: Claims labeled valid or fraud.  

7. Energy Consumption Prediction (Smart Meters)  
Business Impact: Manages electricity distribution more efficiently.  
Model Used: Regression models.  
How Data is Fed: Hourly energy usage table.  
How Training Works: Labeled with future consumption.  

8. Credit Scoring  
Business Impact: Helps banks assess borrower reliability.  
Model Used: Logistic Regression, SVM, XGBoost.  
How Data is Fed: Customer financial data row.  
How Training Works: Labeled with credit score categories.  

9. Product Recommendation (E-commerce)  
Business Impact: Increases sales and customer satisfaction.  
Model Used: Ranking models (XGBoost Ranker).  
How Data is Fed: User-product interaction logs.  
How Training Works: Rows labeled with click/purchase indicators.  

10. ATM Cash Refill Prediction  
Business Impact: Reduces cash shortages and overfill.  
Model Used: Regression models.  
How Data is Fed: ATM withdrawal logs.  
How Training Works: Labeled with required refill amount.

## Label Studio
- open-source data labeling tool  
- used to create training datasets for supervised machine learning   
- for images, text, audio, video, and time-series  
- Faster R-CNN - Annotators draw bounding boxes on images.   
- UNet - Annotators draw pixel masks over tumors, cracks, or objects. 
- CRNN - Annotators highlight text regions and label the text.  
- CNN - Annotators mark time segments in audio. (baby monitors)
- Google, Intel, NVIDIA have confirmed usage of LabelStudio
