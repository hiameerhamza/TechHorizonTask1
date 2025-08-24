# **TechHorizon Internship – Deep Learning Project Summary**

**Intern:** Ameer Hamza
**Date:** August 24, 2025

---

## **1. Project Workflow and Methods**

### **Task 1 – MNIST Digit Classifier**

For the first task, I implemented a feed-forward neural network to recognize handwritten digits. The MNIST dataset (28×28 grayscale images) was loaded through Keras, normalized to a 0–1 range, and reshaped to a one-dimensional vector.
The network consisted of a flattening layer followed by two dense layers (ReLU activation) and a final softmax layer. Adam optimizer and categorical cross-entropy loss were used for training. After about 8–10 epochs, the model produced strong accuracy. Sample predictions were plotted to confirm correctness.

### **Task 2 – Pre-trained Model for Image Recognition**

The second task involved experimenting with transfer learning. I tested **MobileNetV2**, trained on ImageNet, to classify a small collection of diverse images.
Images were resized to match the input requirements (224×224), preprocessed using Keras utilities, and passed through each model. Predictions were decoded and displayed alongside the images, showing label names and confidence scores.
As an extension, I also built a simple app to make the classifier interactive.

### **Task 3 – Interactive Web Application**

As an extension, I built a simple app to make the digit classifier interactive. Using **Gradio**, I created a drawing canvas where users could sketch numbers. The drawn image was converted to grayscale, resized to 28×28, normalized, and then passed to the trained model for prediction. The interface included options to clear and redraw.

---

## **2. Challenges and Solutions**

Task 1 and Task 2 were relatively straightforward to implement, as they mostly involved data preprocessing, model building, and using existing libraries. However, Task 3 was more challenging and time-consuming. Integrating the trained model with a drawing canvas required extra effort; I faced multiple errors while handling the canvas input, preprocessing the sketches, and ensuring compatibility with the model. Debugging these issues took significant time but ultimately improved my understanding of model deployment and user interface integration.

---

## **3. Key Results**

* **Digit Classifier (Task 1):** Typically achieved **97–98%** accuracy on test data. Predicted digits matched well with expected labels on visual checks.
* **Pre-trained Models (Task 2):** MobileNetV2 were able to correctly identify common objects in most test images.
* **Web App (Task 3):** The interface correctly interpreted clear drawings, making the model usable for quick demos.

---

## **4. Learnings and Future Enhancements**

* Dense networks are sufficient for simpler datasets like MNIST, but convolutional layers could boost results further.
* Pre-trained models are a powerful way to tackle small-scale classification problems without heavy training.
* Building even a basic UI requires careful attention to input processing so that the model sees data in the same format as during training.


