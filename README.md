# Deep-Learning-3D

Classify 3d laser-scanned objects with 95% accuracy.

Designed with a Multi-View-CNN architecture, trained on Princeton's modelnet10 data set.

First, convert the volumetric data into discrete voxels:

<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/7.png?raw=true" width="300" height="300">

Then, project the volume into `n` views (`n` is a hyper parameter of the architecture) 

<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/1.png?raw=true" width="150" height="130"><img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/2.png?raw=true" width="150" height="130">
<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/3.png?raw=true" width="150" height="130">
<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/4.png?raw=true" width="150" height="130">
<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/5.png?raw=true" width="150" height="130">
<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/6.png?raw=true" width="150" height="130">

Finally, train a Keras model, that takes the `n` views (photos) as input, and predicts a label.

95% after 18 epochs:

<img src="https://github.com/y0natancohen/Deep-Learning-3D/raw/master/photos/loss_acc.png?raw=true" width="800">
