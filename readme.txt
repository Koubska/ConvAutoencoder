Complete Repo for my studywork.
The final implementation of the convolutional autoencoder can be found in 'Autoencoder_Convolutional.ipynv'
The different architectures can be found in 'Autoencoders.ipynb', where the respective architecuture can be simply copied from and pasted into the right location in 'Autoencoder_Convolutional.ipynb'.

Always make sure to change the name of the model to avoid overwriting the stored model and images and to avoid confusion
I.e. when changing from CR 64to CR32 also change the name "No_Pool_CR_64" to "No_Pool_CR_32", or more simply change every occurence of "CR_64" to "CR_32" in the notebook.

When the model is appropriately named, the already trained model will be loaded automatically and retraining the model is not necessary.
In the stored model the following arguments were used: epochs=100, batch_size=128. Further the models were trained on the dataset 'animal_roberto_ae1.hdf' data with the electrical stimulation points removed.

'mse.txt' contains the mean squared error of each architectures for the validation set, as calculated by the 'Autoencoder_Convolutional.ipynb' notebook.
The notebook 'plots.ipynb' contains the code to plot all different plots used in the presentation and report.

Further, as i own an AMD GPU (Radeon RX 6900 XT) all work was done locally in a dev-container which can be found under the following link: https://hub.docker.com/r/rocm/tensorflow/
This is also why the paths to load the datasets are different and might need to be changed.
At the beginning of the notebooks tensorflow is restricted to only use 12GB out of the 16GB of my GPU, as tensorflow would otherwise use all 16GB and crash my machine.
If this is too much you have to change this value accordingly. In case you reach an OOM error when fitting the network, you can reduce the batch size.