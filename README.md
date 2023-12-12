# Hand_Project
Hand detection using ASL language

**Description**

This code implements a hand gesture recognition system using the OpenCV, cvzone, and Keras libraries. The system detects hand gestures in a video stream and classifies them into 17 different gestures.

**Content**

* **Imports:** The code uses the following libraries:
    * cv2: OpenCV library for computer vision tasks
    * HandDetector: class from cvzone used for hand detection and landmark extraction
    * Classifier: class from cvzone for gesture classification using a pre-trained Keras model
    * numpy: library for numerical operations
    * math: library for mathematical calculations

* **Main Loop:** The code has the following main loop:
    1. **Video capture:** Reads frames from the webcam using `cv2.VideoCapture`.
    2. **Hand detection:** Uses `detector.findHands` to detect hands and extract their bounding boxes and landmarks.
    3. **Crop hand region:** Extracts the hand region based on the bounding box with an offset of 20 pixels.
    4. **Resize and center hand image:** Resizes the hand image to a square size of 300x300 depending on the aspect ratio, while maintaining the aspect ratio and centering it on a white background.
    5. **Prediction:** Uses the `Classifier` class to predict the gesture based on the resized hand image. The prediction result and corresponding index in the labels list are returned.
    6. **Draw bounding box and label:** Draws a rectangle around the hand region and displays the predicted gesture label near the hand.
    7. **Display images:** Shows the original image, cropped hand image, and processed image with the prediction label.

**Notes:**

* The code assumes a pre-trained Keras model and labels file are present in the specified folders ("Model/keras_model.h5", "Model/labels.txt").
* The captured hand region is resized to 300x300 based on the pre-trained model's input size.
* The code currently supports recognizing 17 different gestures represented by the labels list.
* This is a basic implementation of a hand gesture recognition system. The performance can be improved by using more advanced techniques and larger datasets for training the model.

**Generally, the code demonstrates how to build a hand gesture recognition system using the OpenCV, cvzone, and Keras libraries.**

**Additional Explanations**

You can add additional explanations to the description, such as:

* Instructions on how to use the code.
* Suggestions on how to improve or enhance the code.
* Information on the performance of the code.

For example, you can add an explanation like this:

```
**Usage**

To use this code, follow these steps:

1. Install the required libraries:

```
pip install opencv-python
pip install cvzone
pip install keras
```

```
2. Download the recommended model and labels files:

```
wget https://github.com/cvzone/hand-tracking/releases/download/v2.0.0/keras_model.h5
wget https://github.com/cvzone/hand-tracking/releases/download/v2.0.0/labels.txt
```

```
3. Run the code:

```
python hand_gesture_recognition.py
```

```
**Development**

To improve or enhance this code, you can do the following:

* Increase the accuracy and performance of hand gesture detection using more advanced techniques.
* Train the model using larger datasets.
* Explore different applications of hand gesture recognition.
  
**Images**

![Ekran görüntüsü 2023-06-14 111900](https://github.com/serkanyetisen/Hand_Project/assets/64671833/ce74624a-9ac1-49e2-bc35-fca718cc0948)
![Ekran görüntüsü 2023-06-14 111927](https://github.com/serkanyetisen/Hand_Project/assets/64671833/cc7e6b9d-52da-48aa-8d73-411eb861e940)
![Ekran görüntüsü 2023-06-14 111235](https://github.com/serkanyetisen/Hand_Project/assets/64671833/1b3df465-bd9c-426d-aef0-09bded95dd6f)
![Ekran görüntüsü 2023-06-14 111258](https://github.com/serkanyetisen/Hand_Project/assets/64671833/d4b9b2a5-301f-49ab-96bf-333e4abfe318)
![Ekran görüntüsü 2023-06-14 111322](https://github.com/serkanyetisen/Hand_Project/assets/64671833/f1e5cc9e-2050-48a7-9376-d03d15ee55d1)
![Ekran görüntüsü 2023-06-14 111355](https://github.com/serkanyetisen/Hand_Project/assets/64671833/e5244516-7f69-4754-bd81-6829ce6adba7)
![Ekran görüntüsü 2023-06-14 111548](https://github.com/serkanyetisen/Hand_Project/assets/64671833/a373bea8-0b1b-4ffd-ae40-4909335f843c)
![Ekran görüntüsü 2023-06-14 111603](https://github.com/serkanyetisen/Hand_Project/assets/64671833/f6534d43-fa0a-4923-b8e3-c8582aece139)
![Ekran görüntüsü 2023-06-14 111722](https://github.com/serkanyetisen/Hand_Project/assets/64671833/4dda9618-b6ab-4342-8328-e829d3b9b2ff)
![Ekran görüntüsü 2023-06-14 111740](https://github.com/serkanyetisen/Hand_Project/assets/64671833/6721ca96-b105-4bba-96dc-874b1723ec4f)
![Ekran görüntüsü 2023-06-14 111756](https://github.com/serkanyetisen/Hand_Project/assets/64671833/a4b26e75-6ea6-43b1-9149-ec97b67bdf10)
![Ekran görüntüsü 2023-06-14 111808](https://github.com/serkanyetisen/Hand_Project/assets/64671833/29a51cc4-9fd0-4664-abce-67e4298a7c81)
![Ekran görüntüsü 2023-06-14 111824](https://github.com/serkanyetisen/Hand_Project/assets/64671833/3c980135-3db2-4d02-bbe5-45288ea0cc8e)
![Ekran görüntüsü 2023-06-14 111835](https://github.com/serkanyetisen/Hand_Project/assets/64671833/b0d0db02-f6ee-46b8-acc0-142a18d1525e)
![Ekran görüntüsü 2023-06-14 111850](https://github.com/serkanyetisen/Hand_Project/assets/64671833/10220d10-3807-42fc-8fc1-e4f4590bc779)


**Performance**

This code runs in real time and is capable of accurately recognizing 17 different gestures. However, its performance may vary depending on the hardware of the computer being used and the quality of the dataset.


This explanation clearly states how to use and develop the code. It also provides information on the performance of the code.

I hope this is helpful! Let me know if you have any other questions.
