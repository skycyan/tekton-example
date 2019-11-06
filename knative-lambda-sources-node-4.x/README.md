# 参照triggermesh knative-lambda项目：
https://github.com/triggermesh/knative-lambda-runtime

1. 
kubectl -n default create secret generic docker-registry --from-file=.dockerconfigjson=/root/.docker/config.json --from-file=config.json=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson

2.
kubectl apply -f secret-sa.yaml

3.
kubectl apply -f pipelineresources-node4-test.yaml

4.
kubectl apply -f task-node4-runtime.yaml

5.
kubectl apply -f taskrun-node4.yaml
