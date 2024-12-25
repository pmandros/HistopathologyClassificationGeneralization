# Classifying histopathology images with stain augmentations
This notebook investigates the generalization error in machine learning models, focusing on their robustness to variations in data normalization and staining processes. Using the MHIST dataset, a benchmark dataset for histopathological image analysis (https://bmirds.github.io/MHIST/), we employ random staining and normalization techniques to simulate diverse real-world conditions (https://github.com/yiqings/RandStainNA?tab=readme-ov-file). Our findings demonstrate that by introducing randomized staining during the training process, models achieve strong general performance across unseen variations, highlighting the efficacy of this approach in mitigating overfitting and improving model adaptability to unseen data. While this in general known in pathology, we specifically highlight that without this augmentation, the results are **catastrophic**  This work underscores the importance of dataset diversity and preprocessing strategies in building reliable ML systems for computational pathology.

We use a pretrained ResNet18, combined with a Mixture of Experts (MoE) block and a classification layer. We include plots of accuracy, recall, MoE utilization and embedding visualization, and explain predictions with Integrated Gradients. 

