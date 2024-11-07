# Fundamentals of Kuberenetes: YAML Strucuter
> **Prerequisites:** YAML fundamentals. if unfamiliar, checkout [The Basics of YAML in Under 5 Minutes](https://www.youtube.com/watch?v=0fbnyS_lHW4) and [Yaml Tutorial](https://www.youtube.com/watch?v=1uFVr15xDGg&t=528s).

For creating a resource of Kubernetes such as a Pod, Service, Deployment etc, A typical YAML file focuses on 4 Fields:

### `apiVersion`
The `apiVersion` field specifies the version of the Kubernetes API that you’re using to manage this resource. Different resources and Kubernetes versions may require different API versions. 

###  `kind`
The `kind` field tells Kubernetes the type of resource you want to create. For example, A`kind: Pod` means we’re defining a Pod. Kubernetes has various resource types, such as `Service`, `Deployment`, `Job`, etc., each with its specific purpose.

### `metadata`
The `metadata` section provides information to help identify the resource. for example: 
- `name`: This is the unique name of the resource.
- `labels`: Labels are key-value pairs that help categorize and organize resources. Labels can be useful for filtering or grouping resources in a Kubernetes cluster.

### `spec`
The `spec` section defines the desired state of the resource. For Pods, this includes details about containers:
- `containers`: This defines a list of containers that will run within this Pod.
  - `name`: A unique name within the Pod, here `hello-world_container`.
  - `image`: Specifies the container image to use, in this case, `hello-world:latest`.

```
apiVersion: Version fo the API to be used to create resource

kind: type of resource

metadata: information about the resource (below are some of the information that can be passed as metadata)
  name: name of the resource
  labels: tags to help group the resource together, can be more than one
    key: value <- This can be any key-value pair

spec: specifications about the state of resources (below is for a Pod)
  containers: List of Containers
    - name: name of the First Container
      image: Image to be used to create contaner
```
## More:
- [Kubernetes YAML File Explained - Deployment and Service](https://www.youtube.com/watch?v=qmDzcu5uY1I)