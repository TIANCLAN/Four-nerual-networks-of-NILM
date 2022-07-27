# Four-nerual-networks-of-NILM
Four methods of non-intrusive load monitoring: Variational Autoencoder, Denoising Autoencoder, Sequence to Sequence, and Sequence to Point models

##1.Datasets and preprocessing
###it requires the sum and standard deviation of the positve energy of each electrical appliance in the house.
###you can download UKDALE dataset to test and execute the preprocess code:
####python uk_dale_preprocess.py

###if you use other datasets like REDD or REFIT, you can convert them into specific form by using NILMTK.(Distributed with processing code)
###and execute the preprocess code:
####python uk_dale_preprocess.py

##2.Clustering(Optional, distributed with code)

##3.Training and testing

###The training is performed with the following command:

####python NILM_disaggregation.py --gpu 0 --config Config/House_2/WashingMachine_VAE.json
###Where --gpu is used to select a specific GPU, and --config to select the config file associated with the training to execute.

###The test is performed with the following command:

####python NILM_test.py --gpu 0 --config Config/House_2/WashingMachine_VAE.json