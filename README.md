## Tensorflow Server Image for Edge (EAM)

Container image for the [Tensorflow](https://www.tensorflow.org/) server to execute AI Models built with [Kubeflow](https://www.kubeflow.org/).  In particular this image is deployed to Edge Application Manager (EAM) Node(s) as an Edge Service that will execute Tensflow AI Model(s) deployed to it by the EAM Model Management System (MMS).

To support the deployment of Models from EAM, the [MMS Help](https://github.com/TheMosquito/MMS_Helper) functionality is included in this container image.

Software Installed:
*   [Tensor Flow](https://www.tensorflow.org/)
*   [MMS Helper](https://github.com/TheMosquito/MMS_Helper)

## Tensorflow Serving

```
export MODEL_NAME="mymodel"

docker run -t --rm -p 8501:8501   \
-v "$PWD/export:/models/$(MODEL_NAME}" \
-e MODEL_NAME=$(MODEL_NAME} tf-server:v1.0
```
