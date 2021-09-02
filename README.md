## Tensorflow Server Image for Edge (EAM)

Container image for the [Tensorflow](https://www.tensorflow.org/) server to execute AI Models built with [Kubeflow](https://www.kubeflow.org/).  In particular this image is deployed to Edge Application Manager (EAM) Node(s) as an Edge Service that will execute Tensflow AI Model(s) deployed to it by the EAM Model Management System (MMS).

To support the deployment of Models from EAM, the [MMS Help](https://github.com/TheMosquito/MMS_Helper) functionality is included in this container image.

Software Installed:
*   [Tensor](https://www.tensorflow.org/)
*   [MMS Helper](https://github.com/TheMosquito/MMS_Helper)

## Tensorflow Serving

```
docker run -t --rm -p 8501:8501 \
-v "$PWD/export:/models/<model name>" 
-e MODEL_NAME=<model name> edge-tensorflow-runtime:v1.0
```
