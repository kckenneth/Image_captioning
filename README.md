|Title |  Image Captioning |
|-----------|----------------------------------|
|Author | Kenneth Chen, Ph.D |
|Course | w266 NLP Final Project |
|Date | 7/1/2019 |

# Image captioning  
## w266 Final Project (Spring 2019) 
### Kenneth Chen 

This model combines state of the art image classifier, VGG16 with RNN model built with skip-gram approach. 

## Objective 

Be sure to address:
### What do you plan to do? 

I plan to implement two deep networks: CNN and RNN to build the multimodal RNN (MRNN). Image vectors are extracted from the penultimate layer (fc7, fully connected layer) in VGG16 and used as a initial state in RNN GRU nodes. 

### Why is it important, and why is it challenging? 

- It is important because we are entering a new challenging domain where computer vision (CV) and natural language processing (NLP) interacts with each other. Their benefits are manifolds: image retrieval, image captioning for visually disabled persons, surveillance camera etc. 

- It is challenging in many aspects. 
1. First, as a new learner, I need to fully understand how these two models (CNN and RNN) interacts each other within a short period of time. In terms of CNN, there are many CNN models such as LeNet, AlexNet, VGG16, VGG19, Inception3, Xception etc. Recently there have been development of a new model, RPN (Regional Proposal Network). 
2. In terms of RNN in sentence generation, there are many models such as CBOW (Continuous Bag of Words) and skip-gram, i.e., given the target word, the model predict the context word, the approach entirely opposite of CBOW. Deep into the RNN, we'd have a simple RNN or GRU (Gated Recurrent Unite) or LSTM layer, either to keep or forget the prior text information. 
3. The model building is challenging as well because of the large dataset I'm using and GPU implemention in Google Cloud. Each training with adjustment in embedding size, dropout rate to avoid overfitting, multiple recurrent layers takes longer time. 
4. Metric evaluation (Bleu and ROUGE scores) to detect any efficiency in model prediction and human judgement (personally gone through multiple images), cannot implement AMT (Amazon Mechanical Turk) due to time and other personal investment in Google Cloud. 

### What dataset(s) will you use?

- Flickr8k, Flickr30k and MSCOCO 2017 dataset

### What algorithms might you use? Are good implementations available, or will you need to write your own? (Don’t worry if you can’t answer this well at this stage of the course.)

I use CNN (VGG16) and RNN with 3 layers of GRU (512 size in each layer). There are several good implemention of such MRNN for image captioning. However, the novelty is training and validating my model on MSCOCO 2017 dataset instead of MSCOCO 2014 datset. For metric evaluation, I used Bleu and Rouge scores.  

### References to at least four papers related to your proposal

- Karpathy, A. & Li, F.-F. (2014), 'Deep Visual-Semantic Alignments for Generating Image Descriptions.', CoRR abs/1412.2306.

- Kiros, R.; Salakhutdinov, R. & Zemel, R. S. (2014), Multimodal Neural Language Models., in 'ICML' , JMLR.org, , pp. 595-603.

- Lazaridou, A.; Pham, N. T. & Baroni, M. (2015), 'Combining Language and Vision with a Multimodal Skip-gram Model.', CoRR abs/1501.02598.

- Simonyan, K. & Zisserman, A. (2014), 'Very deep convolutional networks for large-scale image recognition', arXiv preprint arXiv:1409.1556.

