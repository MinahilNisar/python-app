#  Python App with CI/CD and Kubernetes

This project demonstrates a dummy Python application containerized using Docker, integrated with a CI/CD pipeline (GitHub Actions), and deployed to a Kubernetes clusterusing **Kind**.

---

## 🧩 Project Structure

python-app/
│
├── app.py # Main Python application
├── requirements.txt # Dependencies
├── Dockerfile # Docker image build instructions
├── deployment.yaml # Kubernetes Deployment manifest
├── service.yaml # Kubernetes Service manifest
└── .github/
└── workflows/
└── main.yml # GitHub Actions CI/CD pipeline


---

##  Technologies Used

- **Python 3.12**
- **Docker**
- **GitHub Actions (CI/CD)**
- **Kubernetes (Kind)**
- **kubectl**

---

##  Steps to Run Locally

###  Clone the Repository
```bash
git clone https://github.com/MinahilNisar/python-app.git
cd python-app

docker build -t python-app .

docker run -p 5000:5000 python-app

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get svc

kubectl port-forward svc/python-app-service 5000:5000


