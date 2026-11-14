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
3. Compare the FP32 and INT8 models using classification accuracy, serialized model size, and CPU inference latency. 
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

The experiments compare the original FP32 model against the INT8 quantized model.

The following metrics are used for evaluation:
1. Accuracy: Classification accuracy on the CIFAR-10 evaluation subset.
2. Model Size: Storage size of the model.
3. Inference Latency: Average time needed to process an image during inference.

# 6. Results Summary

|Metric|FP32 Baseline|INT8 PTQ|
|--|--|--|
|Accuracy|92.40%|92.40%|
|Model Size|42.729 MiB|10.789 MiB|
|CPU Inference Latency|75.255 ms/image|43.433 ms/image|

The results indicate that INT* quantization maintained the baseline classification accuracy in the evaluated experiment. The changes in model size and inference latency are used to assess the resource-efficiency benefits of quantization.

**Note: The complete experimental results, including additional recorded measurements, are available in the `results/` directory.**

# 7. Running the Experiments

The experiments were developed using Jupter notebooks and can be run using Google Colab.

1. Clone or download this repository.
2. Open the `notebooks/` directory.
3. Upload the notebooks to Google Colab or open them in a compatible Jupter environment.
4. Select an appropriate runtime. A GPU runtime is used for consistency with the original experiments, although inference latency is measured on the CPU.
5. Execute the notebook cells in order.

The FP32 baseline notebook evaluates the original model, while the INT8 PTQ notebook performs quantization and evaluates the resulting model.

**Note: The notebooks may require additional package installation or environment configurations before execution. Refer to the setup instructions within each notebook.**

# 8. Conclusion

# 9. Future Work

Future work could investigate full test-set evaluation, lower-bit quantization (e.g. INT4), quantization-aware training (QAT), and deployment on actual embedded edge devices.
