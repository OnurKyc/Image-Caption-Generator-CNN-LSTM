# Image-Caption-Generator-CNN-LSTM

### What is Image Captioning?

Image Captioning is the process of generating textual description of an image. It uses both Natural Language Processing and Computer Vision to generate the captions.Image caption studies based on creation are roughly divided into two: template-based and retrieval-based. Template-based methods that adopt a generative-based approach detect a set of specified visual concepts and create subtitles based on a sentence template or grammar rules (Yang, Y., Teo, C.L., Daume, H., Aloimono, Y., Corpus, 2011), while access-based methods create subtitles from a series of predetermined sentences (Ordonez, V., Kulkarni G., Berg, T.L, 2011). Although both methods produce correct and fluent sentences in terms of grammar, they have some disadvantages and limitations, such as their irrelevant explanations, scope, creativity and complexity of the resulting sentences.

### The CNN-LSTM Model
One of the most interesting and practically useful neural models come from the mixing of the different types of networks together into hybrid models.

![image](https://user-images.githubusercontent.com/72556537/137336560-429061b1-23c9-4f71-b61e-e52cefdee0c4.png)

CNN-LSTM model, specifically designed for sequence prediction problems with spatial inputs, like images or videos. This architecture involves using Convolutional Neural Network (CNN) layers for feature extraction on input data combined with LSTMs to perform sequence prediction on the feature vectors. In short, CNN LSTMs are a class of models that are both spatially and temporally deep and sit at the boundary of Computer Vision and Natural Language Processing. These models have enormous potential and are being increasingly used for many sophisticated tasks such as text classification, video conversion, and so on. Here is a generic architecture of a CNN LSTM Model.

### Feature extraction
The feature extraction model is a neural network that given an image is able to extract the salient features, often in the form of a fixed-length vector. A deep convolutional neural network, or CNN, is used as the feature extraction submodel. This network can be trained directly on the images in your dataset. Alternatively, you can use a pre-trained convolutional model as shown.

![image](https://user-images.githubusercontent.com/72556537/137338096-003a63fb-6e76-4c51-9d07-db5359665442.png)

### Language Model
For image captioning, we are creating an LSTM based model that is used to predict the sequences of words, called the caption, from the feature vectors obtained from the VGG network.

![image](https://user-images.githubusercontent.com/72556537/137338138-1a31ad58-26cc-4860-b267-6efb842af83d.png)


### Encoder
The Convolutional Neural Network(CNN) can be thought of as an encoder. The input image is given to CNN to extract the features. The last hidden state of the CNN is connected to the Decoder.

### Decoder
The Decoder is a Recurrent Neural Network(RNN) which does language modelling up to the word level. The first time step receives the encoded output from the encoder and also the <START> vector.

  
### Proposed Model
  
![model](https://user-images.githubusercontent.com/72556537/137338787-3a8682ab-6ed4-44b1-ae47-bcd888da0cd3.png)
