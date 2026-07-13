I-coolima:Leaf Disease Detection
Author: Samuel Gakuru Wanjohi

About This Project
Hi! Welcome to my project, I-coolima.

In Sub-Saharan Africa, cassava is a super important crop that farmers rely on to feed their families and make a living. But, plant diseases like Cassava Mosaic Disease (CMD) can wipe out a whole farm. Since many farmers live in rural villages, it's hard for them to find an agricultural expert to look at their sick plants.

My goal is to solve this problem using Artificial Intelligence. I am building a tool where a farmer can just take a picture of a sick leaf with their phone, and the AI will tell them exactly what disease it is!

How I Built It
For this project, I used a public dataset from Kaggle containing over 21,000 pictures of cassava leaves. There are 5 categories (1 healthy class and 4 disease classes).

To find the best AI for the job, I ran 8 different coding experiments:

Traditional Machine Learning: I started with older models like Random Forest and SVM. They totally failed because to use them, I had to flatten the images, which destroyed the actual shapes of the spots on the leaves.
Basic Deep Learning: I built my own Convolutional Neural Networks (CNNs). These were better because they could actually "see" the 2D images, but they struggled to learn without memorizing the data.
Transfer Learning (The Winner!): I used a powerful, pre-trained model from Google called Xception. By giving it larger, high-resolution images (224x224), it was finally able to see the tiny yellow veins of the sick leaves.
The Results
My final "Champion" Xception model achieved 79.18% accuracy!

The biggest challenge I faced was that the dataset was super unbalanced (over 13,000 pictures of CMD, but only 1,000 pictures of the rarest disease). To stop the AI from just guessing the most common disease every time, I used a few cool tricks:

Data Augmentation: I wrote code to flip and rotate the images so the AI got to practice looking at different angles.
Class Weights: I mathematically forced the AI to pay more attention to the rare diseases.
Early Stopping & Dropout: I used these techniques to stop the AI from just memorizing the pictures like it was cheating on a test.
What is in this Repository?
i-coolima_notebook.ipynb: This is my main code file. It has all 8 of my experiments, the math, the graphs, and explanations for every step.
Future Plans
Right now, this AI is written in Python using TensorFlow. In the future, I plan to connect this machine learning model to a web app using React and Node.js so farmers can actually use it on their phones!
