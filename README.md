# Virtual-Draping
We present a method to drape a garment from a virtual wardrobe over a 3D body mesh reconstructed from a single image using the SMPL format.

# Introduction
Virtually modelling how 3D garments drape on the human body has widespread applications in the
domains of AR/VR content generation, e-commerce, virtual try-on, gaming, and more.
3D reconstruction of garments with accurate deformations (such as folds and wrinkles) on a custom,
virtual body can help a person infer how a garment might look on their own body. There are several
previous works which employ supervised techniques to learn how clothing deforms as a function of
shape and pose, garment style, and sizing of garments. There are also self-supervised learning
approaches which leverage optimization-based schemes to formulate a set of physics-based loss terms
to train neural networks. 

The goal of this project is to build an end-to-end garment draping pipeline which leverages
self-supervised techniques for redressing garments in 3D on bodies reconstructed from 2D images,
that adapts robustly to changes in pose, shape, garment style and material specifications.

# Methods
We propose a pipeline that consists of three main steps in the following order:
1. 2D image preprocessing with OpenPose to get 2D joints for posing
2. 2D to 3D reconstruction with SMPLify-X, and SMPL body parameter generation
3. 3D garment draping derived from SNUG
