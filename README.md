# AI/ML for 5G-Energy Consumption Modelling by ITU AI/ML in 5G Challenge

## 5G Energy Consumption Modelling
## [Problem Statement](https://zindi.africa/competitions/aiml-for-5g-energy-consumption-modelling)
5G, the fifth generation of radio technology, has brought about new services, technologies, and networking paradigms, with the corresponding social benefits. However, there is growing concern over the energy consumption of these new network deployments. While 5G networks are estimated to be about 4x more energy-efficient than 4G networks, their energy consumption is approximately 3x larger due to the need for a larger number of cells to provide the same coverage at higher frequencies and the increased processing required for wider bandwidths and more antennas.

Base station energy consumption depends on multiple factors, such as specific architecture (e.g. RRU or AAU), configuration parameters (e.g., number of operated carriers, bandwidth, transmit power), traffic conditions (e.g., number of allocated physical resource blocks), and the activation of energy-saving methods (e.g., symbol shutdown, RF shutdown). To reduce network energy consumption, it is crucial to optimize base station parameters and energy-saving methods. This requires a deep understanding of how these parameters and methods impact the energy consumption of different base stations. Therefore, accurate modelling of energy consumption is essential for achieving more energy-efficient network deployments.

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/1943/738561f9-bec5-423d-be50-154fc829046b.png)

## Objective
This ML challenge targets addressing the important questions mentioned above. In the challenge, the participants are asked to design a machine learning-based solution that can be trained on a dataset of few scenarios and then generalize successfully to data from scenarios not seen before. In particular, the designed machine learning model must be able to achieve the following objectives.

* **Objective A:** Develop a model able to estimate the energy consumed by different base station products. The participants are required to develop a model that estimates the energy consumed by different base station products, taking into consideration the impact of various engineering configurations, traffic conditions, and energy-saving methods.

* **Objective B:** Achieve generalization capabilities across different base station products. The model must estimate the energy consumption of a new base station product based on measurements collected from existing ones, such as Products A, B, and C. For example, if training data is available for these three products, the model must be able to provide an estimate of the energy consumed by Product D.

* **Objective C:** Achieve generalization capabilities across different base station configurations. The model must predict the energy consumption of newly configured parameters based on a small number of real network configuration parameters. For instance, if the training data contains samples collected from many base station products, when the transmit power is set to 30, 35, and 43 dBm, the model must estimate the energy consumed when the transmit power is set to 40 dBm.

## Metrics
To focus on the cross-equipment and cross-configuration generalization capability of the model, the test set estimation accuracy is evaluated by using a weighted relative error evaluation method. Specifically, the error weight, w_i, of the sample corresponding to the new device and/or new configuration in the test set is larger and is provided in the test set.

The final model performance is ranked according to the **minimum WMAPE error**

![](https://zindi-public-release.s3.eu-west-2.amazonaws.com/uploads/image_attachment/image/1944/584d2bb7-8d36-4a32-91b2-4ce603be6bbf.png)
