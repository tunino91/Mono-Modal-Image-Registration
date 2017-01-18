# Mono-Modal-Image-Registration

Implement a deformable image registration method (use ITK algorithms or your own developed algorithms integrated into ITK path) to register two thoracic CT scans. Accurate registration of thoracic CT is both extremely useful in clinical terms and exceptionally challenging due to the elastic nature of lung tissue deformations. Note that two thoracic CT scans should belong to the same subject; hence, it is mono-modal image registration. As for 
#### Similarity function: MattesMutualInformationImagetoImageMetric
#### Registration: ImageRegistrationMethod
#### Optimizer: RegularStepGradientDescentOptimizer 
are general functions used from itk library.

This example illustrates a realistic pipeline for solving a full deformable registration problem. 
First the two images are roughly aligned by using a transform initialization, then they are registered using a rigid transform, that in turn, is used to initialize a registration with an affine transform. The transform resulting from the affine registration is used as the bulk transform of a BSplineTransform. The deformable registration is computed, and finally the resulting transform is used to resample the moving image.

# Results
<img width="1291" alt="before-afterreg" src="https://cloud.githubusercontent.com/assets/19553239/22082491/e9982494-dd95-11e6-8dc1-8dc2968e91a1.png">
