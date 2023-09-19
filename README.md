# Exploring-Semi-Supervised-and-Active-Learning-Techniques-in-Data-Analysis

Semi-supervised learning and active learning approaches offer interesting avenues to explore when the data to which we have access are only partially labeled. These two types of strategies make it possible to take advantage of the information contained in unlabeled data in order to improve the performance of the final model. The first propose to incorporate this information within the training or the structure of the model, while continuing to exploit the labeled data as is the case in standard supervised learning. The second assumes that an oracle will be able to label a portion of the samples in a cyclical manner, and guides the selection of samples to be labeled, preferring those which will promote a significant improvement of the model.

The content of this work is primarily based on an article written by Ms. Mathilde Galinier on April 29, 2022, which can be found at the following link: https://www.aquiladata.fr/insights/semi-supervised-learning-active-learning-comment-tirer-profit-des-donnees-non-labellisees.

The sole purpose of the produced work is to present different techniques. It is by no means intended to achieve extraordinary performance improvements. In fact, even the case chosen is not particularly complex for applying these techniques with the goal of enhancing performance.




- ***Semi-Supervised Learning Techniques***:

**Self Training**: also known as pseudo labeling, is a semi-supervised learning technique where a model is trained on the available labeled data and then used to predict labels for unlabeled data. These pseudo-labeled predictions are then added to the labeled dataset to retrain the model.


**Co-Training**: is a semi-supervised learning approach that involves two models, each trained on a different subset of the available data. These models complement each other by labeling the most uncertain unlabeled data instances for each other. This approach is based on the assumption that different models can provide complementary information.


**Labeling with Generative Models**: Labeling with generative models involves using generative models, such as GANs (Generative Adversarial Networks), to assist in the labeling of unlabeled data. These generative models can generate synthetic labeled data points, helping to expand the labeled dataset.

**Labeling with Graphs**: Labeling with graphs is a semi-supervised learning technique that leverages the relationships between data points represented as a graph or network structure. It involves propagating labels through the graph based on the labels of neighboring data points, enhancing the labeling process.


- ***Active Learning Techniques***:

**Uncertainty**: In AL, uncertainty-based sampling selects data points for labeling that the model is uncertain about. This uncertainty is typically measured using metrics such as entropy or prediction probability. It aims to reduce model uncertainty by focusing on informative data points.

**Diversity**: Diversity-based active learning aims to select diverse data points for labeling. Instead of focusing solely on uncertainty, it seeks to include different data representations in the labeled dataset, enhancing model robustness and generalization.

**Expected Change with EGL (Expected Gradient Length)**: Expected Change with EGL is an active learning strategy that evaluates the potential impact of labeling specific data points. It calculates the expected change in the model's gradient magnitude when a data point is labeled, considering both class probabilities and gradient directions. It selects data points likely to bring significant model improvement.
