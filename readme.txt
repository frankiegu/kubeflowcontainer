v1.2.0
FROM quay.io/datawire/ambassador:0.30.1
FROM quay.io/datawire/statsd:0.30.1
FROM gcr.io/kubeflow/jupyterhub-k8s:1.0.1
FROM gcr.io/google_containers/spartakus-amd64:v1.0.0
FROM gcr.io/kubeflow-images-staging/tensorflow-1.4.1-notebook-cpu:v20180403-1f854c44
FROM gcr.io/kubeflow-images-staging/tensorflow-1.4.1-notebook-gpu:v20180403-1f854c44
FROM gcr.io/kubeflow-images-public/tf-model-server-cpu:v20180327-995786ec
FROM gcr.io/kubeflow-images-public/tf-model-server-gpu:v20180327-995786ec
FROM gcr.io/kubeflow-images-public/tf-model-server-http-proxy:v20180327-995786ec
FROM gcr.io/kubeflow-images-staging/tf_operator:v20180329-a7511ff
FROM gcr.io/tf-on-k8s-dogfood/tf_sample:dc944ff

FROM gcr.io/tf-on-k8s-dogfood/tf_sample_gpu:dc944ff




docker pull quelle/tensorflow-1.7.0-notebook-gpu:latest
docker tag quelle/tensorflow-1.7.0-notebook-gpu:latest  gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-gpu:latest
docker save -o gcr.io-kubeflow-images-public-tensorflow-1.7.0-notebook-gpu_latest gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-gpu:latest

docker pull quelle/issue-summarization-ui:0.1
docker tag quelle/issue-summarization-ui:0.1 gcr.io/gcr-repository-name/issue-summarization-ui:0.1
docker save -o gcr.io-gcr-repository-name-issue-summarization-ui_0.1 gcr.io/gcr-repository-name/issue-summarization-ui:0.1
docker pull quelle/kubeflow-download:latest
docker run -it -v



FROM gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-cpu:latest


v0.2.0
image: gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1
image: seldonio/cluster-manager:0.2.1
image: redis:4.0.1
image: gcr.io/kubeflow-images-public/tf_operator:v20180724-13863edf
image: quay.io/datawire/ambassador:0.37.0
image: quay.io/datawire/statsd:0.37.0
image: argoproj/workflow-controller:latest
image: argoproj/argoui:latest
image: gcr.io/kubeflow-images-public/centraldashboard:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-cpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-gpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.7.1-notebook-cpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.7.1-notebook-gpu:v0.2.1

docker pull quelle/statsd:v0.37.0
docker pull quelle/ambassador:v0.37.0
docker pull quelle/jupyterhub-k8s:v20180531-3bb991b1
docker pull quelle/tf_operator:v20180724-13863edf
docker pull quelle/centraldashboard:v0.2.1
docker pull quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker pull quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1

docker save -o  quelle-statsd-0.37.0.tar quelle/statsd:v0.37.0
docker save -o  quelle-ambassador:0.37.0.tar quelle/ambassador:v0.37.0
docker save -o  quelle-jupyterhub-k8s:v20180531-3bb991b1.tar quelle/jupyterhub-k8s:v20180531-3bb991b1
docker save -o  quelle-tf_operator-v20180724-13863edf.tar quelle/tf_operator:v20180724-13863edf
docker save -o kubeflow-tensorflow-1.4.1-notebook-cpu-v0.2.1.tar quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker save -o kubeflow-tensorflow-1.4.1-notebook-gpu-v0.2.1.tar  quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1

docker load -i kubeflow-tensorflow-1.4.1-notebook-cpu-v0.2.1.tar
docker load -i kubeflow-tensorflow-1.4.1-notebook-gpu-v0.2.1.tar
docker  load -i  quelle-statsd-0.37.0.tar 
docker  load -i  quelle-ambassador:0.37.0.tar 
docker  load -i  quelle-jupyterhub-k8s:v20180531-3bb991b1.tar 
docker  load -i  quelle-tf_operator-v20180724-13863edf.tar 

docker  tag quelle/statsd:v0.37.0   quay.io/datawire/statsd:0.37.0
docker  tag quelle/ambassador:v0.37.0 quay.io/datawire/ambassador:0.37.0
docker  tag quelle/jupyterhub-k8s:v20180531-3bb991b1   gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1
docker  tag quelle/tf_operator:v20180724-13863edf  gcr.io/kubeflow-images-public/tf_operator:v20180724-13863edf
docker  tag quelle/centraldashboard:v0.2.1 gcr.io/kubeflow-images-public/centraldashboard:v0.2.1
docker  tag quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1 gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker  tag quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1 gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-gpu:v0.2.1






