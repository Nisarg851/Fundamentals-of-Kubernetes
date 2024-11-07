### Fundamental Lab: Creating a ReplicaSet with YAML Configuration

**Objective:** To understand the process of defining a ReplicaSet, the pod template, and the selector.

**Tasks to be Completed:**

1. **Create the ReplicaSet YAML File**:
   - Define a YAML file that creates a ReplicaSet with the following specifications:
     - **Name**: `first-replicaset`
     - **Replicas**: 2
     - **Label Selector**: `tags: Fundamental`
     - **Pod Template**:
       - **Name**: `my-pod`
       - **Labels**: `tags: Fundamental`
       - **Containers**:
         - **Name**: `my-container`
         - **Image**: `hello-world:latest`

2. **Apply the YAML Configuration**:
   - Use the `kubectl apply` command to create the ReplicaSet in your Kubernetes cluster using the YAML file you’ve defined.

3. **Verify ReplicaSet Creation**:
   - Use `kubectl get rs` to check the status of the newly created ReplicaSet and ensure it is running with the specified number of replicas.

4. **Check Pod Creation**:
   - Verify that the appropriate number of pods are created under the ReplicaSet by running `kubectl get pods`. Ensure that the pods have the correct labels (`tags: Fundamental`).

5. **Scale the ReplicaSet**:
   - Modify the ReplicaSet to scale up or down the number of replicas. Apply the updated YAML file and check that the number of pods matches the new replica count.

6. **Inspect the ReplicaSet**:
   - Use the `kubectl describe rs` command to inspect the ReplicaSet details. Verify that the ReplicaSet’s selector and pod template are configured as expected.

7. **Delete the ReplicaSet**:
   - Use the `kubectl delete rs` command to delete the ReplicaSet and clean up the resources.

