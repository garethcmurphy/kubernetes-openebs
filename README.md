# Kubernetes OpenEBS Setup 🛠️📦  

This repository provides a setup for deploying and managing **OpenEBS** on a Kubernetes cluster. OpenEBS enables dynamic, container-attached storage for stateful applications.

---

## Features ✨  

- **Dynamic Storage**: Provision and manage persistent volumes with OpenEBS.  
- **Kubernetes Native**: Fully integrated with Kubernetes for seamless workflows.  
- **Storage Classes**: Create custom storage classes for applications.  
- **Scalable Solution**: Suitable for various stateful workloads.  

---

## Prerequisites 🛠️  

- A running Kubernetes cluster.  
- Kubernetes CLI (`kubectl`) configured.  
- Helm installed for chart-based deployments.  

---

## Installation  

1. Clone the repository:  
git clone https://github.com/your-username/kubernetes-openebs.git  
cd kubernetes-openebs  

2. Install OpenEBS using Helm:  
helm repo add openebs https://openebs.github.io/charts  
helm repo update  
helm install openebs openebs/openebs --namespace openebs --create-namespace  

3. Verify the installation:  
kubectl get pods -n openebs  

---

## Configuration  

- **Storage Classes**:  
  Modify the `storageclass.yaml` file to define custom storage policies.  

  Apply the storage class:  
  kubectl apply -f storageclass.yaml  

- **Volume Provisioning**:  
  Update the application's PersistentVolumeClaim (PVC) to use the OpenEBS storage class.  

---

## Monitoring  

1. Check OpenEBS components:  
kubectl get pods -n openebs  

2. View logs for debugging:  
kubectl logs <openebs-pod-name> -n openebs  

3. Verify provisioned volumes:  
kubectl get pv  

---

## File Structure 📂  

- `storageclass.yaml`: Sample storage class for OpenEBS.  
- `README.md`: Documentation for the repository.  

---

## Example Commands  

- Install OpenEBS:  
  helm install openebs openebs/openebs --namespace openebs  

- Apply storage class:  
  kubectl apply -f storageclass.yaml  

- List provisioned volumes:  
  kubectl get pv  

---

## Contributing 🤝  

1. Fork the repository.  
2. Create a new branch:  
git checkout -b feature/your-feature  

3. Commit your changes:  
git commit -m "Add your feature"  

4. Push the branch:  
git push origin feature/your-feature  

5. Open a pull request.  

---

## License 📝  

This project is licensed under the MIT License. See the LICENSE file for details.  

---

**Deploy scalable and dynamic storage with OpenEBS on Kubernetes!** 🛠️📦  
