# OCR-gpu-to-cpu 

This project focuses on optimizing Optical Character Recognition (OCR) models, specifically EasyOCR, to run efficiently on CPU while maintaining accuracy and performance. The goal was to demonstrate how a model typically optimized for GPU can be adapted for CPU usage, which is crucial for applications where GPU resources are limited or unavailable.
Key Components
1. Performance Comparison
The project includes a simulated comparison of GPU and CPU performance in terms of:

Processing Time: The time taken for the OCR model to process an image.
Accuracy: The percentage of correctly recognized characters.
Resource Utilization: The CPU and GPU resource usage during the OCR processing.

2. Techniques for Optimizing OCR Models for CPU
To enhance the performance of the OCR model on a CPU, the following techniques were implemented:

Quantization: This technique reduces the precision of the model's weights from floating-point (32 bits) to lower-bit representations (e.g., 8 bits). This decreases model size and increases inference speed, albeit with a potential trade-off in accuracy. (We have used this).

Batch Processing: When processing multiple images, batch processing can significantly reduce the overhead of loading the model multiple times and improve overall throughput.

3. Strategies to Maintain Accuracy and FPS
To ensure that the model maintains a high level of accuracy and frames per second (FPS) during CPU operation, the following strategies were utilized:

Fine-Tuning: Fine-tuning the model on a specific dataset helps it learn task-specific features, leading to improved accuracy. This can involve training the model on a labeled dataset that reflects the specific types of text and images it will encounter, allowing for a more tailored performance while maintaining reasonable processing speeds.(We have used this).

Optimized Preprocessing: Efficient image preprocessing techniques were applied to ensure that the input images are suitable for the model, thereby reducing the likelihood of misrecognition. This includes resizing images to the appropriate dimensions, normalizing pixel values, and applying filters to enhance text visibility.

Result:- Performance Comparison:
CPU Processing Time: 0.85 seconds
CPU Accuracy: 98.87%
CPU Resource Utilization: 77.08% (CPU), 0.00% (GPU)

GPU Processing Time: 0.85 seconds
GPU Accuracy: 98.20%
GPU Resource Utilization: 92.32% (CPU), 64.09% (GPU)
getting optimized result.
