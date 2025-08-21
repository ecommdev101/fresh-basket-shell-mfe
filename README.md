# fresh-basket-shell-mfe
apiVersion: apps/v1
kind: Deployment
metadata:
  name: docker-demo
spec:
  replicas: 1
  selector:
    matchLabels:
      app: docker-demo
  template:
    metadata:
      labels:
        app: docker-demo
    spec:
      containers:
      - name: docker-demo
        image: 590181219128.dkr.ecr.ap-south-1.amazonaws.com/docker-demo:v1
      imagePullSecrets:
      - name: ecr-secret
