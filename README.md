# CustomizedRBFKernelGraphCut-Paper-With-Code
Customized RBF Kernel Graph-Cut for Weak Boundary Image Segmentation

This repository presents an implementation of the Radius-based Function (RBF) Kernel Graph Cut algorithm, which has shown promising results in image segmentation tasks. However, traditional RBF approaches struggle to accurately segment images with weak boundaries, such as cellular images, where distinguishing regions with narrow and close boundaries is challenging.

The ideal kernel is the one that not only compresses energy in each region, but also distinguishes unrelated features well from each other. Image features can be implicitly mapped to higher dimensions using the kernel.
In the RBF kernel graph-cut algorithm, the RBF kernel is defined based on the exponential function. In order to define the proposed kernel, the above kernel is decomposed into two sine and cosine functions based on the Euler equation. Discrete Cosine transform (DCT) is a, unitary, orthogonal and energy compressor transformation. For this reason, the cosine kernel can distinguish regions well within narrow boundaries. The sine kernel is orthogonal to the cosine kernel and can provide a homogeneous space for segmentation. Because the homogeneity of regions and the quality of their boundary are dissimilar in different images, sine and cosine kernel fusion with appropriate weight are desirable. 
Image energy varies from zero to one depending on the complexity of the image. In homogeneous images with weaker boundaries, the lower frequency components are stronger and therefore the total energy is higher. In contrast, the presence of strong boundaries in the image can divide the homogeneous region into smaller regions and reduce the total energy. This energy is calculated based on the sum of the squares of the components in the Gray level co-occurrence matrix 
Given that the image energy can be a suitable factor to determine the degree of weakness of image boundaries and its complexity, the sine and cosine discrete terms in the proposed kernel are fused based on the amount of the image energy. 


If you find this work useful in your research, please consider citing the following paper:
M. Niazi, K. Rahbar, M. Sheikhan, and M. Khademi, "Customized RBF kernel graph-cut for weak boundary image segmentation," Signal, Image Video Process., pp. 1–9, Mar. 2023.

You can access the paper at https://link.springer.com/article/10.1007/s11760-023-02546-7
