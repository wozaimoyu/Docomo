# Deep Learning Coordinated Beamforming for Highly-Mobile Millimeter Wave Systems
This is a MATLAB code package related to the following article:
Ahmed Alkhateeb, Sam Alex, Paul Varkey, Ying Li, Qi Qu, and Djordje Tujkovic, "[Deep Learning Coordinated Beamforming for Highly-Mobile Millimeter Wave Systems](https://arxiv.org/abs/1804.10334)," in IEEE Access, vol. 6, pp. 37328-37348, 2018.
# Abstract of the Article
Supporting high mobility in millimeter wave (mmWave) systems enables a wide range of important applications such as vehicular communications and wireless virtual/augmented reality. Realizing this in practice, though, requires overcoming several challenges. First, the use of narrow beams and the sensitivity of mmWave signals to blockage greatly impact the coverage and reliability of highly-mobile links. Second, highly-mobile users in dense mmWave deployments need to frequently hand-off between base stations (BSs), which is associated with critical control and latency overhead. Further, identifying the optimal beamforming vectors in large antenna array mmWave systems requires considerable training overhead, which significantly affects the efficiency of these mobile systems. In this paper, a novel integrated machine learning and coordinated beamforming solution is developed to overcome these challenges and enable highly-mobile mmWave applications. In the proposed solution, a number of distributed yet coordinating BSs simultaneously serve a mobile user. This user ideally needs to transmit only one uplink training pilot sequence that will be jointly received at the coordinating BSs using omni or quasi-omni beam patterns. These received signals draw a defining signature not only for the user location, but also for its interaction with the surrounding environment. The developed solution then leverages a deep learning model that learns how to use these signatures to predict the beamforming vectors at the BSs. This renders a comprehensive solution that supports highly-mobile mmWave applications with reliable coverage, low latency, and negligible training overhead. Extensive simulation results, based on accurate ray-tracing, show that the proposed deep-learning coordinated beamforming strategy approaches the achievable rate of the genie-aided solution that knows the optimal beamforming vectors with no training overhead, and attains higher rates compared to traditional mmWave beamforming techniques.
# Code Package Content 
The main script for generating the following figure.
![Figure7](https://github.com/WSLCL/DeepLearning-CoordinatedBeamforming/blob/master/Result_BF.png)
This script adopts the publicly available parameterized [DeepMIMO dataset](http://deepmimo.net/ray_tracing.html) published for deep learning applications in mmWave and massive MIMO systems. The 'O1' scenario is adopted for this figure.

**To reproduce the results, please follow these steps:**
1. Download the "BeamPrediction_Signature.zip" file, expand/uncompress it, and then add the folder to the "DeepMIMO_Dataset_Generation" folder. (Note that both the DeepMIMO dataset generation files and the source data of the 'O1' scenario are available on [this link](https://github.com/DeepMIMO/DeepMIMO-codes)).
2. Run the file named `DL_CoordinatedBeamforming.m` in MATLAB to generate the inputs/outputs of the deep learning model.
3. Run the file named `DLmodel_python_code.py` to build, train, and test the deep learning model. This step requires Python 3.6, Keras, and Tensorflow.
4. Run the file named `Figure_Generator.m` in MATLAB to process the deep learning outputs and generate the performance results/figures.

If you have any questions regarding the code and used dataset, please contact [Ahmed Alkhateeb](http://www.aalkhateeb.net/).
# License and Referencing
This code package is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). If you in any way use this code for research that results in publications, please cite our original article:

> A. Alkhateeb, S. Alex, P. Varkey, Y. Li, Q. Qu and D. Tujkovic, "[Deep Learning Coordinated Beamforming for Highly-Mobile Millimeter Wave Systems](https://arxiv.org/abs/1804.10334)," in IEEE Access, vol. 6, pp. 37328-37348, 2018.