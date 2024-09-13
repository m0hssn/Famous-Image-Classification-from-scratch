# CNN Architectures with PyTorch

## Overview

This repository contains implementations of two popular Convolutional Neural Network (CNN) architectures: **GoogLeNet (Inception V1)** and **ResNet34**. Both architectures are implemented in PyTorch and trained on the CIFAR-10 dataset.

### GoogLeNet (Inception V1)

GoogLeNet, introduced in 2014, marked a significant advancement in CNN architecture by winning the ILSVRC 2014 image classification challenge. Key innovations include:

- **1x1 Convolutions**: Reduces the number of parameters and computational load.
  
  ![Example Image](https://media.geeksforgeeks.org/wp-content/uploads/20200429201100/without1x1.png)
  
  - **Operations without 1x1 convolutions**: 112.9M
  - **With 1x1 convolutions**: 5.3M
  
- **Global Average Pooling**: Reduces the dimensionality of feature maps, which enhances accuracy.

- **Inception Modules**: Combine multiple convolutional and pooling operations to capture features at different scales.

  ![Conv Layer](https://media.geeksforgeeks.org/wp-content/uploads/20200429201304/Incepption-module.PNG)

- **Auxiliary Classifiers**: Intermediate classifiers that aid training by combating vanishing gradients and providing regularization.

  ![Google-Net](https://media.geeksforgeeks.org/wp-content/uploads/20200429201549/Inceptionv1_architecture.png)

### ResNet34

ResNet34 introduces residual connections to address the vanishing gradient problem in deeper networks. This architecture allows for very deep networks without suffering from diminishing gradients.

- **Residual Connections**: Enable gradients to flow through the network more effectively by providing shortcuts around some layers.

  ![Residual connection](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnh652pYukUxlSOAMl60YafqG7gln6rXujSwfz3G0b0PUw9mbqpGTz-TXJmpkib_6rSGs&usqp=CAU)

## Notes

- **Auxiliary Classifiers**: They are included in GoogLeNet to improve training but can be omitted if not needed.
- **Memory Considerations**: For ResNet34, batch size adjustments might be required depending on the available memory.

## References

- **GoogLeNet (Inception V1)**: [Going Deeper with Convolutions](https://arxiv.org/abs/1409.4842)
- **ResNet34**: [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
