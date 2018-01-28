[http://ruder.io/optimizing-gradient-descent/

[https://www.linkedin.com/pulse/chapter-12-gradient-descent-math-madhu-sanjeevi/

Great contribution from OpenAI: TensorFlow code for Gradient Checkpointing.

One frequent bottleneck in deep learning is memory. For example, some of my students working with medical imaging have mammographies of up to 5,000 x 5,000 pixels. Trying to feed them into their convolutional neural net results in memory errors. Downsampling them results in a huge loss of accuracy. Their solution was to chop them into patches, but this is still not ideal because of losing signal about global structure and symmetry.

GPU RAM is increasing very slowly (say, cards of today have ~25% more RAM than those of 4 years ago).

Gradient checkpointing is neat: it allows O(sqrt(n)) memory use vs O(n) with vanilla backprop. With only a ~20-30% computation penalty, authors were able to fit a 10x larger model onto their GPUs.

The idea is simple: instead of keeping in memory all activations to compute backprop, some checkpoints are kept in memory and the other activations recomputed when needed.

The speed penalty is small because accessing RAM is expensive anyway and recomputing activations is relatively cheap.

Check it out on GitHub: https://lnkd.in/enamPng

*** Bagging (Bootstrap Aggregation): Basics ***
~ Invented by Leo Breiman: Bootstrap aggregation.
~ L. Breiman, "Bagging predictors," Machine Learning, 1996.
~ Majority vote from classifiers (models, algorithms) trained on bootstrap samples of training data.
~ Bagging:
1. Generate B bootstrap samples of the training data: random sampling with replacement.
2. Train a classifier or a regression model using each bootstrap sample.
3. For classification: majority vote on the classification results. 
4. For regression: average of predicted values.
5. Error variation is reduced, not so for error bias. 
6. Suitable for high variance low bias models (complex models)
7. Improves performance of unstable classifiers with small changes in the dataset. 
8. Found trees improve a lot (Random Forests)
9. Works because averaging over bootstrap samples reduces error variance, especially with unstable classifiers. 
10. Bagging is a powerful technique. Explore it. Enjoy it. See Comment A. 
--- B. Noted
