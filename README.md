# Hard_nut_to_crack
The notebook is about improvement of classification accuracy for hard items in FashionMNIST dataset using random erase for regularization.

Previous results (see FM_SG.ipynb in my repository FashionMNIST_Image_Classification) indicate that 4 of the item classes - 0: T-shirt/top, 2: Pullover, 4: Coat, and 6: Shirt - are harder to classify; test accuracy for these items
are about 89%, while other items are classified with about 98% accuracy.

In the notebook HardRandomEraseFM.ipynb we use random erase method for regularization and train 5 models for 100 epochs to investigate whether classification accuracy
for these hard classes can be improved.

We find that this approach increases classification accuracy for these hard to classify items from 89% to 93.5%

### Observations:
A simple CNN can achieve classification accuracy of over 93%.
Combining 3 models improves accuracy around 94.4%

It takes around 16 seconds per epoch using Colaboratory GPU accelerator and Test accuracy does not improve significantly after the first 20 epochs.

Combining a few more models trained over 20 epochs may further improve classification accuracy in a resonable amount of time.

Classification accuracy is significantly lower for 4 classes: 'T-shirt/top', 'Pullover', 'Coat', and 'Shirt'

### Opportunities for improvement:
Devise alternate methods for combining models

Increase the diversity of constituent models

Introduce regularization methods that prevent over-fitting beyond 20 epochs

Develop a two-phased approach: Predict using a combination of models in the first phase and use a separate model to re-classify examples predicted as 'T-shirt/top', 'Pullover', 'Coat', or 'Shirt
