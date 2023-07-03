# Deployment between the cloud and bare metal

- Kubernetes is way easier to deploy and maintain than some years ago
- For local development testing there is https://kind.sigs.k8s.io/docs/user/quick-start/
- For deploying stuff at the edge there is https://kubeedge.io/en/docs/
- The big issue about deploying at the customer's infrastructure is the expectation management. It needs to be clear, who is responsible for which part of the deployment process.
- If the customer is not willing to provide you with the infrastructure you need or is not willing to pay for maintenance and service, you should reconsider working with them.
- In cases where the customer does not have the requirements for a real "cluster" solution, bare metal or just podman/docker ist fine.
- Work with an expert, it might not be necessary to put k8s to your Fullstack-List
- https://www.replicated.com tries to solve the problem to deploy to k8s-infrastructure at different clients (but is quite pricey 😮‍💨)