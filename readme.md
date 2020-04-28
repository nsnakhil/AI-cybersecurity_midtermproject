# Cloud-based PE Malware Detection API 
### The purpose of this term project is to demonstrate your practical skills in implementing and deploying machine learning models for malware classification. The technical implementation of this project is comprised of three main tasks that need to be completed sequentially:

Task 1 - Training: In this task, you will be creating and training a deep neural network based on the
MalConv architecture to classify PE files as malware or benign. As for the dataset, you will be using the
EMBER-2017 v2 ( https://github.com/endgameinc/ember ). Besides the references provided in this
repository, the following two talks at BSides San Francisco 2018 and the CAMLIS 2019 conferences
present detailed overviews of this dataset, as well as hints on how to use EMBER to train malware
classifiers:

 https://youtu.be/TzW_R36iv48
 https://www.youtube.com/watch?v=MsZmnUO5lkY

If you explore the EMBER repository, you will find that it comes with a sample implementation of
MalConv ( https://github.com/endgameinc/ember/tree/master/malconv ). This sample is a wonderful
resource to base your implementation on. However, note that this code is 2 years (i.e., a lifetime in ML)
old, and does not precisely conform to the requirements of this project.

 Implementation: The model must be implemented in Python 3.x using TensorFlow (1.x or 2.x)
and Keras, and needs to be coded and documented in a Jupyter Notebook. You can work in
native Python for coding and testing the model if you wish, but afterwards you will need to
convert your Python code into a Jupyter notebook. Similar to the notebooks we’ve seen in the
exercises, you must also add textual description blocks to the notebook to document and
explain the different parts of your code.

 Training: This model may take a long time to train on your personal computers (from 7-8 hours
to a couple of days, depending on the config), unless you already have a powerful NVIDIA GPU
(1080 TI or better). Alternatively, you can use the following cloud platforms to speed up the
training:
o Google Colab
o Amazon AWS Sagemaker

 Post-Training: Once your model is trained, save and store the model. Then, create a function (or
method) that takes a PE file as its argument, runs it through the trained model, and returns the
output (i.e., Malware or Benign).

Task 2 - Deploy your model on the cloud: In this task, you will be using Amazon Sagemaker to
deploy your model on the cloud, and create an endpoint (~ API) so that other applications can make use
of the model. While this might sound very complicated, you will find that it is actually quite simple to
deploy models using Sagemaker. To learn about the procedure, you can follow this tutorial:
 Video: https://youtu.be/8ygCyvRZ074
 Jupyter Notebook:
https://github.com/jeffheaton/t81_558_deep_learning/blob/master/t81_558_class_13_02_cloud.ipynb

Task 3 – Create a client: This task is quite simple as well: create a Python code that loads a PE file,
converts it into a feature vector that is compatible with your MalConv/EMBER model, runs the vector on
the cloud API, and then prints the results (i.e., Malware or Benign – or probabilities of each). You can
find a sample implementation here: https://github.com/endgameinc/ember/tree/master/malconv

##### Check out this link for my report - https://github.com/nsnakhil/AI-cybersecurity_midtermproject/blob/master/Cloud-based%20PE%20Malware%20Detection%20API.docx 
