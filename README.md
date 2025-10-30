# Unsupervised-Learning-Models---NY-Property-Tax-Fraud---PCA---Autoencoder
NY property tax fraud project description:
The dataset contains 1 million record, and 32 variables like lot, market values, tax classes. I used unsupervised anomaly detection because the fraud is unusual which makes it a good case for unsupervised learning. The most important part is to build the right space, where outlier is meaningful to the problem.

Looking for unusual valuation on the fields FULLVAL, AVLAND, and AVTOT. Normalize by lot area, building area etc. Remove correlation by applying PCA. 
Then, apply 2 outlier detection methods:
1. Zscale - all the dimensional are scaled and centered, then distance to origin
2. Autoencoder - functional mapping of a record back to itself. The records have larger error are unusual records.
Neither of its own would be a good meausure, so I’ll combine the results to get the final anomaly score
