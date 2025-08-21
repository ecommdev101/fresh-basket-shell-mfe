# fresh-basket-shell-mfe
apiVersion: v1
kind: Service
metadata:
  name: docker-demo-service
spec:
  type: LoadBalancer
  selector:
    app: docker-demo
  ports:
    - protocol: TCP
      port: 80
      targetPort: 9200
