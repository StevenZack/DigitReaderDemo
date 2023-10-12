# Instructions

1. Install docker

```
sudo apt install docker.io
```

2. Install minikube
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start
```

3. Train our model

```
sudo apt install python3-pip
pip install tensorflow numpy mnist keras
```

train our model
```
python3 train.py
```

4. Create an API service

Install FastAPI 
```
pip install fastapi "uvicorn[standard]" Pillow
```

5. Build Docker image
```
docker build -t zigzigcheers/digitreader:v1 .
```

test if it works
```
docker run -d -p 8080:8080  zigzigcheers/digitreader:v1 
```

6. Deploy to Kubernetes Cluster

```
kubectl create deployment digitreader --image=zigzigcheers/digitreader:v1
kubectl expose deployment digitreader --type=LoadBalancer --port=8080
```

7. Next steps

Using AWS service to make it work

- [Amazon Polly](https://aws.amazon.com/polly/?nc2=type_a)
- [Amazon Translate](https://aws.amazon.com/translate/?nc2=type_a)
