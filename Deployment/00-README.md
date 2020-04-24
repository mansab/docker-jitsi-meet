- Modify the DOCKER_HOST_ADDRESS env value in 01-Deployment.yaml
- kubectl create ns jitsi
- kubectl create secret generic jitsi-config -n jitsi --from-literal=JICOFO_COMPONENT_SECRET=... --from-literal=JICOFO_AUTH_PASSWORD=... --from-literal=JVB_AUTH_PASSWORD=..
- kubectl apply -f (Link to 01-Deployment.yaml)

- To update the logo:

Obtain the logo (don't push to this repo)

Delete existing configmap
```
kubectl delete configmap jitsi-icon -n jitsi
```

Create new configmap using new logo icon
```
kubectl create configmap jitsi-icon --from-file=watermark.png -n jitsi
```

Then restart the pod
