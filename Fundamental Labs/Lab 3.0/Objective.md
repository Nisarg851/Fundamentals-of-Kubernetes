### Kubernetes Deployment Lab: Fundamentals of Creating a Deployment with YAML

**Objective:** To understand the process of defining a Deployment, the pod template, and the selector.

**Tasks to be Completed:**

1. **Create a Deployment YAML file**:  
   - Define a **Deployment** with the name `first-deployment`.
   - Specify the **replicas** field to 2, ensuring two replicas of the pod are created.
   - Set the **selector** with a label `tags: Fundamental` to match the pods controlled by the deployment.

2. **Define the Pod Template**:
   - In the pod template, set the **metadata** to include a label `tags: Fundamental`.
   - Set the **name** of the pod to `my-pod`.
   
3. **Create the Container Specification**:
   - In the pod template, define a container within the spec.
   - Name the container `my-container`.
   - Set the **image** of the container to `hello-world:latest`.

4. **Apply the YAML file to create the Deployment**:
   - Apply the YAML file using `kubectl apply -f <filename>.yaml` to create the deployment in the Kubernetes cluster.

5. **Verify the Deployment**:
   - Check the status of the deployment to ensure that the desired number of replicas (2) are running.
   - Ensure the pods are successfully created and are in the **Running** state.

6. **Scale the Deployment**:
   - Scale the deployment up or down by modifying the `replicas` field in the YAML file and applying the change.

7. **View Pod Logs**:
   - Access the logs of the containers running in the deployed pods to verify they are working as expected.

8. **Delete the Deployment**:
   - Delete the deployment using `kubectl delete deployment <deployment-name>` and verify that the pods are deleted.
