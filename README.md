# envoy-apigateway
envoy-apigateway deployment and configuration scripts

# post api gateway deployment

kubectl get svc -w  --namespace caliber ambassador

export SERVICE_IP=$(kubectl get svc --namespace caliber ambassador -o jsonpath='{.status.loadBalancer.ingress[0].ip}')

echo http://$SERVICE_IP
