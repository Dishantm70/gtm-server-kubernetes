# gtm-server-kubernetes

A simple helm chart to deploy GTM server side tagging server on Kubernetes.

Deploying the tagging server on Kubernetes requires two main resources. A Deployment resource to run the GTM server docker container in a pod and a LoadBalancer Service resource to publicly expose the deployment on a stable IP address.
## Steps
* Replace the containerConfig variable at the end of the values.yaml file with your GTM container config string.
* Install the helm chart.

        helm install gtm-server .
* Get the public IP address of your service.

        kubectl get service gtm-server

That's it! You can now access the GTM server on the service's IP address. Map your tagging domain name with the IP address.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
MIT
