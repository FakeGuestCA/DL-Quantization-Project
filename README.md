# CMPE 401-Self-defined-Project
# Evaluating Post-Training INT8 Quantization of ResNet-18 for Efficient Deep Learning Inference
Group member(s): Trevor Wu (79013249)

# 1. Project Overview

This project investigates the effects of post-training quantization (PTQ) on deep learning model performance, focusing on resource-constrained inference.

Using a ResNet-18 image classification model trained on the CIFAR-10 dataset, the project evaluates the trade-offs between model accuracy, model size, and inference latency when converting a full-precision (FP32) model to an 8-bit integer (INT8) quantized model.

The primary objective is to determine whether quantization can reduce model resource requirements while maintaing classification accuracy.

# 2. Objectives

1. Establish a baseline using the original FP32 ResNet-18 model.
2. Apply INT8 post-training quantization to reduce model size and computational requirements.
3. Compare the FP32 and INT8 models using classification accuracy, serialized model size, and inference latency. 
4. Evaluate the effectiveness and limitations of PTQ for resource-constrained deployment.

# 3. Model and Dataset

|Component|Description|
|--|--|
|Model architecture|ResNet-18|
|Pretrained model|SamAdamDay/resnet18_cifar10|
|Dataset|CIFAR-10|
|Task|Image classification|
|Baseline precision|FP32|
|Quantized precision|INT8|
|Evaluation images|1,000|
|Random seed|42|

Note that the pretrained ResNet-18 model is obtained from Hugging Face and evaluated using the CIFAR-10 dataset.

# 4. Directory Description

1. `notebooks/`: Contains the Jupter notebooks for the FP32 baseline evaluation and INT8 post-training quantization experiments.
2. `results/`: Contains the JSON files storing the experimental results for each model.
3. `CMPE 401 Self-defined Project Technical Report`: Documents the project methodology, experimental results, and analysis.
4. `CMPE 401 Self-defined Project Video`: Provides a brief overview of the project, apporach, results, and conclusions.

# 5. Experimental Results

# 6. Results Summary

# 7. Running the Experiments

# 8. Conclusion

# 9. Future Work
