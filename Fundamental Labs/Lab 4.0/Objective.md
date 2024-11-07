### Fundamental Lab: Creating a Kubernetes Service with YAML

**Objective:** To understand how to define and set up a service to expose an application within the cluster.

**Tasks to be Completed:**

1. **Define the Service**:
   - Create a new YAML file named `first-service.yaml` that defines a Kubernetes **Service** with the following attributes:
     - `apiVersion`: v1
     - `kind`: Service
     - `metadata`: Set the `name` to `first-service`.
     - `spec`: Configure the following elements:
       - **selector**: Use a label selector to target pods with the label `tags: Fundamental`.
       - **type**: Set the service type to `ClusterIP`.
       - **ports**: Define the port configuration to:
         - Expose port `80` on the service.
         - Map `targetPort` to `80` (the port that the container is listening on).

2. **Create a Deployment to Expose the Service**:
   - Create a simple pod or deployment that has a container listening on port 80.
   - Label the pods with `tags: Fundamental` to ensure the service can target the right pods.

3. **Apply the YAML File**:
   - Use `kubectl` to apply the YAML file and create the Service in your Kubernetes cluster.

4. **Verify the Service**:
   - Use `kubectl get services` to confirm that the service was successfully created and is running.
   - Check that the service is correctly routing traffic to the target pod.

5. **Test the Service**:
   - Access the service using the pod's internal IP within the cluster.
   - Verify that the service correctly routes traffic to the backend pod’s container on port 80.

6. **Clean Up**:
   - After the testing is complete, delete the service and any related resources (such as the pod or deployment) using `kubectl delete`.