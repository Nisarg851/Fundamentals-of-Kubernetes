### Fundamental Lab: Creating a Pod with YAML Configuration

**Objective:** Practice creating a Kubernetes pod using a YAML configuration file.

**Tasks to be Completed:**

1. **Create YAML File**:
   - Write a YAML configuration file to define a pod.
   - Ensure the pod name is set to `First-Pod`.
   - Assign the label `tags: Fundamental` to the pod.

2. **Define Container Configuration**:
   - Set the container name to `hello-world-container`.
   - Specify the container image as `hello-world:latest`.

3. **Apply YAML Configuration**:
   - Deploy the pod to the Kubernetes cluster using the created YAML file.

4. **Verify Pod Creation**:
   - Check that the pod `First-Pod` is running successfully in the cluster.
   - Confirm that the pod has the label `tags: Fundamental`.

5. **Check Pod Status and Details**:
   - Retrieve and review the details of `First-Pod` to confirm the container name, image, and assigned labels.

6. **Delete the Pod**:
   - Delete `First-Pod` from the cluster and verify it has been removed. 
