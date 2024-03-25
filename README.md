# Sample-difficulty-estimation-with-action-scores-for-various-NLP-tasks

## Background

Biases in AI systems compromise model interpretability, fairness, and reliability. These biases, often stemming from skewed or unrepresentative training data, can lead to models that misinterpret or struggle with certain samples, obscuring the understanding of their decision-making processes. Furthermore, biases can result in DNNs predicting uncalibrated confidences, which, especially in sensitive applications, can lead to misguided decisions with potentially catastrophic outcomes. Addressing these biases is essential to ensure that AI models are both equitable and trustworthy. One way to delve deeper into the model’s explainability is through estimating the difficultness of learning a particular sample. There are already many techniques that assess these properties of the data but they are either computationally complex or their application is restricted to specific tasks [[3]](#references). A more robust and multi-purpose unsupervised method has recently been introduced to evaluate the difficulty of machine learning models by calculating a difficulty score based on the accumulated loss per epoch [[2]](#references). This method, which does not necessitate any model modifications or external supervision, has been tested on tasks like image classification, segmentation, and object detection. However, its application and implications for Natural Language Processing (NLP) tasks remain unexplored.

## Research question

This project aims to extend the application of the action score method, primarily used in image-based tasks, to various NLP tasks, including sentiment analysis, summarization, and question answering. I am going to implement separate models for each task and apply the proposed method together with other quantitative metrics that assess sample difficulty such as variance of gradients [[1]](#references) and considering different training dynamics [[4]](#references) and do a comparative analysis. Further, I am going to test whether this method would be effective as a human auditing tool for detection of incorrectly labeled samples and apply curriculum learning based on action scores. Given the aforementioned structure of the proposed project, the research question is as follows:

**Can the action score measure difficulty in natural language processing tasks?**

## References

[1] Chirag Agarwal and Sara Hooker. “Estimating Example Difficulty using Variance of Gradients”. In: CoRR abs/2008.11600 (2020). arXiv: 2008.11600. URL: [https://arxiv.org/abs/2008.11600](https://arxiv.org/abs/2008.11600).

[2] Octavio Arriaga, Sebastian Palacio, and Matias Valdenegro-Toro. “Difficulty Estimation With Action Scores for Computer Vision Tasks”. In: Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) Workshops. June 2023, pp. 245–253.

[3] Fredrik K. Gustafsson, Martin Danelljan, and Thomas B. Schön. Evaluating Scalable Bayesian Deep Learning Methods for Robust Computer Vision. 2020. arXiv: 1906.01620 [cs.LG].

[4] Swabha Swayamdipta et al. “Dataset cartography: Mapping and diagnosing datasets with training dynamics”. In: arXiv preprint arXiv:2009.10795 (2020).


