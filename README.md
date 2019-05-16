# Hard_nut_to_crack
The notebook is about improvement of classification accuracy for hard items in FashionMNIST dataset using random erase for regularization.

Previous results (see FM_SG.ipynb in my repository FashionMNIST_Image_Classification) indicate that 4 of the item classes - 0: T-shirt/top, 2: Pullover, 4: Coat, and 6: Shirt - are harder to classify; test accuracy for these items
are about 89%, while other items are classified with about 98% accuracy.

In the notebook HardRandomEraseFM.ipynb we use random erase method for regularization and train 5 models for 100 epochs to investigate whether classification accuracy
for these hard classes can be improved.

We find that this approach increases classification accuracy for these hard to classify items from 89% to 93.5%
