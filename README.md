# Image captioning  
## w266 Final Project (Spring 2019) 
### Kenneth Chen 

This model combines state of the art image classifier, VGG16 with RNN model built with skip-gram approach. 

## Objective 

Be sure to address:
### What do you plan to do? 

I plan to implement two deep networks: CNN and RNN to build the multimodal RNN (MRNN). Image vectors are extracted from the penultimate layer (fc7, fully connected layer) in VGG16 and used as a initial state in RNN GRU nodes. 

### Why is it important, and why is it challenging? 

- It is important because we are entering a new challenging domain where computer vision (CV) and natural language processing (NLP) interacts with each other. Their benefits are manyfolds: image retrieval, image captioning for visually disabled persons, surveillance camera etc. 

- It is challenging with many aspects. 
1. First, as a new learner, I need to fully understand how these two models (CNN and RNN) interacts each other. In terms of CNN, there are many CNN models such as LeNet, AlexNet, VGG16, VGG19, Inception3, Xception etc. Recently there have been development of a new model, RPN (Regional Proposal Network). 
2. In terms of RNN in sentence generation, there are many models such as CBOW (Continuous Bag of Words) and skip-gram, i.e., given the target word, the model predict the context word, the approach entirely opposite of CBOW. Deep into the RNN, we'd have a simple RNN or GRU (Gated Recurrent Unite) or LSTM layer, either to keep or forget the prior text information. 
3. 

### What dataset(s) will you use?

### What algorithms might you use? Are good implementations available, or will you need to write your own? (Don’t worry if you can’t answer this well at this stage of the course.)

### References to at least four papers related to your proposal
